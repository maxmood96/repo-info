## `amazoncorretto:21-alpine3.23-jdk`

```console
$ docker pull amazoncorretto@sha256:cfe5f26dc4a56f65a37f1a9f251c41c5d8a7cbcd21e4073edeb7dd9071eb0d1b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e7e43f8855f9980799ae535c1ea7b4e9d0d2bb2ec8b31dbc34c622e30874dfb3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165657668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d399765ee59d8b7eb9977e8b8f05595a0798d4c991c2d48b9006aafedcf89d4a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:14 GMT
ARG version=21.0.11.10.1
# Mon, 22 Jun 2026 19:54:14 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:54:14 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:54:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4ec98a16ff123b525fabd6d8724084cfa4f15d646b1d0b4d8facd391fed5cd8`  
		Last Modified: Mon, 22 Jun 2026 19:54:35 GMT  
		Size: 161.8 MB (161813247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:411ef1d1a3c50160395faede3f4dabdd2b2b44c659c238e17ee3d0dd061b473a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.8 KB (591783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8df4cc095eb835c23d2160cc4cd58112872328ea019e2bae713545968b20f0`

```dockerfile
```

-	Layers:
	-	`sha256:e9613400bd4a950c09849e05c6cd583fc7bc3306e4642e622dbc73441144339d`  
		Last Modified: Mon, 22 Jun 2026 19:54:29 GMT  
		Size: 582.4 KB (582406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:484991134a8c80979599103fa9355a848e6c4afb00663a1f657bd5fd6ab01080`  
		Last Modified: Mon, 22 Jun 2026 19:54:29 GMT  
		Size: 9.4 KB (9377 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7ca10bc73d266ff5e529ad35e7be703c17c45264b63f581929babaeec109223d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164010470 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e002d93846d446f9b320db23483edd1ae89c030c7e8c690a7327faf817946e5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:43 GMT
ARG version=21.0.11.10.1
# Mon, 22 Jun 2026 19:55:43 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:55:43 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:55:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7ff8f47fab236078ab9f635ab55d8fcfb9775daec3653a92a0e85ad17f5678`  
		Last Modified: Mon, 22 Jun 2026 19:56:02 GMT  
		Size: 159.8 MB (159828610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:978cf836643708a5da9d46b09dd1aa306675da425083ff942283ac2f54ec1482
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.7 KB (590658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65882755b5c318ac88a58792cb60e900480a23ba2775de677e75106b7daa4fa0`

```dockerfile
```

-	Layers:
	-	`sha256:f3827734bdc41cafd8fb8f2df73c0e68268db6c70f7db6163928b9e0d940bf2f`  
		Last Modified: Mon, 22 Jun 2026 19:55:59 GMT  
		Size: 581.2 KB (581175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e2df6361d5bca488ad13913397457685727fdad41ea2b3b6cfd737b692cbe7`  
		Last Modified: Mon, 22 Jun 2026 19:55:59 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
