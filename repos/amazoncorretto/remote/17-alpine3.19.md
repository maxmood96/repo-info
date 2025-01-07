## `amazoncorretto:17-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:337be09b8a321ba5a14cd02592469b6bcc217a93943fa2f4a15c944bccb7b388
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:45b392eb082c71e8aa8b1bfd414c5475e1507276a8320785d9241c4acaaa61c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149062686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf429289e85bcbcb55d2c1f55819c022fd384b8abb55ae7581e3552917293272`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=17.0.13.11.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a1e253e3a28c952791becb5d8dc116a50846d17a8dff4355b5b0771f1c9045`  
		Last Modified: Tue, 07 Jan 2025 03:30:21 GMT  
		Size: 145.6 MB (145649415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7f4667b2a7fff9fe7cc993e0d12d334a85de674d97aa4344f50576143551b3cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.3 KB (390315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403acea3558a71279b24e384711e76bd3f4b8ad1771ca3cc5e9058df6aa3808d`

```dockerfile
```

-	Layers:
	-	`sha256:ca8b33a1055c943979981abd01e66eea7fd32e0bfe423398fb770bfc6ea5bf20`  
		Last Modified: Tue, 07 Jan 2025 03:30:17 GMT  
		Size: 380.9 KB (380895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a388d800673100b66bfaaab3e74a2bd414bccc9afddd38814b2c80696da9516`  
		Last Modified: Tue, 07 Jan 2025 03:30:17 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:26f1aa9ff3b2955359507203453aaa165aaaeb1e346398cc7b3c6e28acdae8a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.3 MB (147294336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2325786d362c917e610085689fe8d0c0ec1f47aca2fcf0144161b491ed2617d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b9d09d3cf7c289c838a14468f834bc8a42a5648a603618dd9b71ef5b453d04`  
		Last Modified: Wed, 13 Nov 2024 07:53:53 GMT  
		Size: 143.9 MB (143935090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:31ea9b3cb6130c8e2d6d03d29fc41881b8d4ea99e220a9f4911f6b9d38e9be47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.5 KB (390468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b9072511c1d908cde4583f84264d181dc21deabbc9e5ba6aa08126c095a9fd9`

```dockerfile
```

-	Layers:
	-	`sha256:785fb80fbd48f66c02735110131a9c9653f2dc6856e3ca71c9187d77a69d1af4`  
		Last Modified: Wed, 13 Nov 2024 07:53:49 GMT  
		Size: 380.9 KB (380942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d3ff5af9c9c10c8d0aafed636f57e7b1fd8ee1a62ccba0c95d0ac3f99edf8ab`  
		Last Modified: Wed, 13 Nov 2024 07:53:48 GMT  
		Size: 9.5 KB (9526 bytes)  
		MIME: application/vnd.in-toto+json
