## `amazoncorretto:23-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:435451882b9a07c1c0f077053ac22861915d64e0bb95f26466d0255c2101c8ec
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
		Last Modified: Fri, 14 Feb 2025 19:12:58 GMT  
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
$ docker pull amazoncorretto@sha256:88838d570ca5935d68cc0a3612595a0a3d60162ef02b30e83eb401e754df812f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167750697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3dbe9637def7f24bfca9e2eb723563090024ff885be40fb4b5b8f63e22feb5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f667f42a5367d609333da21f1ce59f892b560125d6b7b1a7adcd3b0c4e1165e`  
		Last Modified: Thu, 23 Jan 2025 18:57:00 GMT  
		Size: 164.4 MB (164408836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:38810bde38843647f90d9ae78b3e94e5ba9bedceeeab8f774429abe06bdd9373
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.4 KB (390375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d2b2019d9d05f0d58eaedcb05cc3f284a11b47771a1d36ebdd05e88fd36a186`

```dockerfile
```

-	Layers:
	-	`sha256:eada28e2e9c91007467c479351e047f5df4a9bf5aa256d0bf3488960d9179584`  
		Last Modified: Fri, 14 Feb 2025 22:49:17 GMT  
		Size: 380.9 KB (380857 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa5ffaa3ade52568a84b6f2e1a5e4689f77eaf5bddc5b2dcd019e62a49b4de17`  
		Last Modified: Fri, 14 Feb 2025 22:49:17 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
