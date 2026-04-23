## `amazoncorretto:21-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:eb03c85f01df9be41dafbc3f89d8d64a6de1bdb52580ebf6e05439273a11fb28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cdd730bad190e8e17909e687c8d042c7ab521826d034a574ca169b3c9522e44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165433636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20711e45669cd61b3d0222fa5c91d8d707068c2df8c06bf5031c852e67965b2e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:48 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:48 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:48 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:48 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:48 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6777afa599a4887f471994b014c50c9ab366e003d50d12b2735b7c7f95528eb0`  
		Last Modified: Wed, 22 Apr 2026 21:35:07 GMT  
		Size: 161.8 MB (161803315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e80314abde23b6e18a528018f2f0762e27fba3f614240646eaff2ccc448d189f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.6 KB (590581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3d812e3511d1999aad68e53a9a64b89bd0d72327caf15da65275c51e39986f1`

```dockerfile
```

-	Layers:
	-	`sha256:a62da836983187d12732556d5f77d0382da480ffe667e076dcd5b6e34b77cc0e`  
		Last Modified: Wed, 22 Apr 2026 21:35:04 GMT  
		Size: 581.2 KB (581203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:165d20eeee81fdec83cf4a2a563aeee3ecee653261eb2a681d0b5c9605d41f46`  
		Last Modified: Wed, 22 Apr 2026 21:35:04 GMT  
		Size: 9.4 KB (9378 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0943738f745a075cc3c1c006cf98438648029ba1395a535c18b1fb562ceac7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.9 MB (163926509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efbb74ae4eb80b901fb85db487e9a577b4ad4684c81ef7b885045a8bc0c04153`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:42 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:42 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:42 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b272f7833143a48c1d7b6f6b3cc5a3988806f1ba70d4cd6d9490f2bcaf4df9`  
		Last Modified: Wed, 22 Apr 2026 21:35:05 GMT  
		Size: 159.8 MB (159834190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f9ba30f7e4d22a186c4abd2de49896fac52d09e1978f449b0404ed5d3bcd907b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.1 KB (590104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ce0181ce0f535c3cd564f4940a3c5c7758543d8fe5f87f4c409b095974416d`

```dockerfile
```

-	Layers:
	-	`sha256:fb6613d206900b093b7d6d770b8bac265fc23b6daeb7ce0aeca7cef2bb059c59`  
		Last Modified: Wed, 22 Apr 2026 21:34:59 GMT  
		Size: 580.6 KB (580622 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04ae97f58fcc3874fd63b947c85d97ce65ef3e2c21bdcf6e4261251f897bf878`  
		Last Modified: Wed, 22 Apr 2026 21:34:58 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json
