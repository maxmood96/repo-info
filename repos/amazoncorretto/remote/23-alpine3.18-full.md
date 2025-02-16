## `amazoncorretto:23-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:a9a83a7bec78989eaa0660bf30f153de06ff3be14ed5b527b0f9f2f13e32917f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.18-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:32aeeadc6afef1b6f91ad208ec357bbe03e9daf59b9c8e597190eb222b2688d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170106699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91980d5bfaa0105bcce39fe77ac00441de24572515f4956cdad5b519be8c5646`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 14:36:09 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef35e065db5480379e73b4d52bab0986e765398337e5a82ac591d025086bf4da`  
		Last Modified: Sat, 15 Feb 2025 05:56:58 GMT  
		Size: 166.7 MB (166688290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a390103419620d6731e154f3f7105efce242226571f76c63e953a3422ce22161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.5 KB (391492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfaac603cd832f0a97235986d4ca8619195ce6647d1cabbb87d6ed2d20e2de23`

```dockerfile
```

-	Layers:
	-	`sha256:f35ac0a4a3b93e45e7935f1e0cc8dbd3726f49fcfbf9b438831d262c99498205`  
		Last Modified: Fri, 14 Feb 2025 22:49:15 GMT  
		Size: 382.1 KB (382078 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e9a5b503f69117b8dd7027c30dc6cf4a74dac21c935f6a2f634712e03443d9a`  
		Last Modified: Fri, 14 Feb 2025 22:49:15 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f9df886e4772c0f79947a5adc4e65306710fdd629739b050d6b6e4fe0239cd5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167751510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbd0df9852c1ec78c1f06f37931b36869c95a149771a78b57e5aca13ca26ec77`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 14:36:47 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7ff19c574d11aef36f44ca306ba780ff40cfc816220582fa8d656bf268c383f`  
		Last Modified: Sun, 16 Feb 2025 14:20:37 GMT  
		Size: 164.4 MB (164408853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a97eca28a2b03431127c518f96f9000310d47a6591e9737d7adf5ee3c3e32a51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 KB (390374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d590a9d49486abc2fcd9378c2b827ab458e27a59e029be6139fa5803b65444`

```dockerfile
```

-	Layers:
	-	`sha256:4a20aedaa1a58154cb51230b52256ba49dd805e35a501f509afd5802b1987097`  
		Last Modified: Sat, 15 Feb 2025 01:49:09 GMT  
		Size: 380.9 KB (380857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d6e16de13d5e466e60368f08a2a6fff5e87fe4a1931ae08c0ecbefb33c9c58e0`  
		Last Modified: Sat, 15 Feb 2025 01:49:09 GMT  
		Size: 9.5 KB (9517 bytes)  
		MIME: application/vnd.in-toto+json
