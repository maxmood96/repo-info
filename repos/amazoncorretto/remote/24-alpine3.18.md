## `amazoncorretto:24-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:d81628b9c3712956cfcf868f4048da804a70462234196f8c8d704dd84c95c66d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b16cc5a4949a7a89bd9540bb0a80c21919cb197ca419ef84e230ad4c1c5f9c35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180022751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c1bd9ac91639efc11187a81f73c7089d04da05c1a81d99142b852a06a31d342`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:03:06 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 14:36:09 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711523ee11395cdb8034c90428a453cc06abf8c0e58feee6e7f4fe10e6b0cd1b`  
		Last Modified: Thu, 08 May 2025 17:13:18 GMT  
		Size: 176.6 MB (176604342 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a4c703d5fda0f076b010c16b5e9e98982e2a3578bf461c4b1549490c7014693b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.6 KB (398637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90af3b1419d1ff779a54ee8a942af390fe5655c0d83340a659a8aeefbfd0180`

```dockerfile
```

-	Layers:
	-	`sha256:9e8c0be168ae1a0b39f15371500bb2db4d88dff44f6da1d5d2c71dda2ec4bb2c`  
		Last Modified: Tue, 15 Apr 2025 23:56:07 GMT  
		Size: 389.2 KB (389223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85b9497d8cbbf9f135235891bf3871dd5351b9a969389755de589725792b535`  
		Last Modified: Tue, 15 Apr 2025 23:56:07 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:884489a3142181abfe18a59735a1a68ad6e83aa3b3c5fa71c4f9c52345853530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.6 MB (177645088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3941e159f29931b714c088a63937507d915341015a932d7954609033959d5cc1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:03:06 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 14:36:47 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a1c4b2163789f75cd0b96be80df4fc88498a5d771033a115fd35d935ccc27a1`  
		Last Modified: Wed, 16 Apr 2025 00:23:43 GMT  
		Size: 174.3 MB (174302431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eca715017be43496e3f5e68afb6f41461af5368dd1020e5d4a3f24ab1bac1fe0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.2 KB (398157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a58d6bac7c08a740a7ea86451939d5e781391c91d1ffa11da529fdb97f164585`

```dockerfile
```

-	Layers:
	-	`sha256:2a14d6d7ae4ce6fb824effff3ce785fe45f78fe224142b3b13e947c91690f922`  
		Last Modified: Wed, 16 Apr 2025 00:23:38 GMT  
		Size: 388.6 KB (388639 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91db887492f58442ba4a2a2509f859428b8ca8fd2757ce0f8aa9175a0571b69b`  
		Last Modified: Wed, 16 Apr 2025 00:23:38 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
