## `amazoncorretto:8-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:85a25a3a9622da652a9e43e4816bf9874c76c21d8261b42a121cdce86228de15
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7d1c8b9e359b5d7d57172334c0d37b5ecaf4bcb24cf505edd21938833f553747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45072742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f311f45feec310eb62497d27d15f4e24ed2d2c65e46891005fe2702ea37bf8d1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c3125bc4877cbabee024089a757ea1f36ca7db3381c60c71d32bb5f02929e8a`  
		Last Modified: Fri, 14 Feb 2025 19:24:29 GMT  
		Size: 41.7 MB (41654333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb8aea5cc98f29e18faa4fa66c3ca90f3e0889e44b318cc35a598eabb5750ef8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.4 KB (193371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e739d2cfb7b24692d1359e9d61ed5b69c7172b8f6bb00f3db8c220a6530eaf63`

```dockerfile
```

-	Layers:
	-	`sha256:0806f8992c0d07241688d489ee7d6b5bfc4a9fd1a6848bb3788d0b24dcd393bb`  
		Last Modified: Fri, 14 Feb 2025 19:24:29 GMT  
		Size: 184.7 KB (184672 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a38fb0c375c15068db04b664cf653bbc67f07e3e0ea5c3a5cedfac087ec42a5c`  
		Last Modified: Fri, 14 Feb 2025 19:24:29 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a43efea5a96c576544900584ea84d9281fcd41abd720f634494bdfbbf2d1803b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44704662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32de47cd678f3d89d6a7d71cd40eeae20ac570594f35593a6394cce5ab1d23d5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 12:05:04 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caf128ae164aeed8e6719c696ac3907b13e92e2cecdf43e25263428d1b150036`  
		Last Modified: Fri, 14 Feb 2025 22:31:37 GMT  
		Size: 41.4 MB (41362005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1096f1bdc950d0a55ccfa0f92ee526b05716086a1f85dd876887bcada4253a04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cec89b864e8fd55564f590c0bc67b93096de1cc864a41bb7e70c8c45d88d879`

```dockerfile
```

-	Layers:
	-	`sha256:c52cff8f5dba2f47a610945681a922d90bce78b077e0dd04db0ea93b1eddab6a`  
		Last Modified: Fri, 14 Feb 2025 22:31:23 GMT  
		Size: 184.8 KB (184780 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0866c2bc648917874ec8ecef2a41b4b9fbeeba502f2954e22372209216810156`  
		Last Modified: Fri, 14 Feb 2025 22:31:23 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
