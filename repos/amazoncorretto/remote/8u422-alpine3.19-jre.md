## `amazoncorretto:8u422-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:a881e3bb7a8209c4e9bd2bf0fabb807c6d153be9cd1c07d4663d411aef7c08da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:47d53fae3224e89d9bebd88b5e76f96a9adbfacff996eebb39da523b5cb60e91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45016692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59910d7b86a676b5b76c7fa44601d26086e61c9596dd517bc68fa49b0fefc354`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:17:04 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Thu, 20 Jun 2024 20:17:04 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10a635e9b5a0ecd3a5aeccf82d9567c1a84d2a0000c9dc3e0f90dcc59cf307be`  
		Last Modified: Thu, 18 Jul 2024 00:55:29 GMT  
		Size: 41.6 MB (41599360 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0bc37ef39f1e990483b2fdd88e8a9c376f008ca098d39e0489e666465d5519f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 KB (193839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a73cca0cd3cc33fd14aceef7251c591b5604d82805e345a90d1a36b577d26a`

```dockerfile
```

-	Layers:
	-	`sha256:58cf193dd434db8dc532c6974017e4091df677150ba8ed6f6c36f9fa7e4bb282`  
		Last Modified: Thu, 18 Jul 2024 00:55:28 GMT  
		Size: 185.4 KB (185386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170d4a609f421525413473f718b76d88a524aa8b69f1c9e75f235cabb242b263`  
		Last Modified: Thu, 18 Jul 2024 00:55:28 GMT  
		Size: 8.5 KB (8453 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:412334418d51f9ef51b55f4e4a0d75456e4e03743e4ca55c8e8f46c50a695396
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44663590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce1fd40e2977938caaa78b51aee26e3f60428ac6d96d38aa145fe06dc3d3c4b4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:38 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Thu, 20 Jun 2024 17:40:38 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876bb239e45afdadd4848e7335a223a5b66c928e95bd8045340c5202b2e564ce`  
		Last Modified: Thu, 18 Jul 2024 01:00:51 GMT  
		Size: 41.3 MB (41306388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4b490dcdd4611381a93eb6c4725c0bae6eb58599453dfed39916896d1deb478f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b3d5d0abeebe599e4ea6ad3a1107196de88affe89ae543e90926bb8d0b6bb75`

```dockerfile
```

-	Layers:
	-	`sha256:db2bc373a1fc81a8bf9ff656dee51c8b69109c3b7dffc880d7aa10016c33bcad`  
		Last Modified: Thu, 18 Jul 2024 01:00:49 GMT  
		Size: 185.5 KB (185494 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:399952c87d185d1d7ad06e0ed669e105160794dc3f0941b23b198d65557b7d64`  
		Last Modified: Thu, 18 Jul 2024 01:00:49 GMT  
		Size: 8.7 KB (8730 bytes)  
		MIME: application/vnd.in-toto+json
