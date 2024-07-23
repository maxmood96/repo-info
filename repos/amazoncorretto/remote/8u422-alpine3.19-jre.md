## `amazoncorretto:8u422-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:9e68e1e86f325cb18b19229e192022411a79cbf7dc73543eea7bb10025d8124f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ae72b90c40be91f72b800cff3f3e1e63bb260215d4d2fc58618cee1421eb999e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45018454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e7b464eff0b39f057b41fbc5f32d1e6502ca0c18cf123fb3aff4aedcc4c0184`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c644b15c170e2ca46176a566910d40a21dce66518ed8fdfd34ebcf0e9dc90c55 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
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
	-	`sha256:46b060cc26202cf98e28414d790b5cabd67094bba50315a1ae2e9daf913fca4f`  
		Last Modified: Mon, 22 Jul 2024 22:27:25 GMT  
		Size: 3.4 MB (3419040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da3e4b582d4020819801a28793afe31df4dce59e98a1ef117ec217374425f59c`  
		Last Modified: Mon, 22 Jul 2024 23:04:22 GMT  
		Size: 41.6 MB (41599414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:865d84cbb70ececddaf3802bd118ea9ea8ea96c3b3d4d5051619e16f1ca2c64b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 KB (193840 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bffa37e2eb8ea44fc658fb6a6c7765e78ecea95d26c79ca99c426a3cb821f00a`

```dockerfile
```

-	Layers:
	-	`sha256:4e4f1fcc1607ee570a382374cefa3fac5d251b170a0a5f18dc32f21a80ae232c`  
		Last Modified: Mon, 22 Jul 2024 23:04:21 GMT  
		Size: 185.4 KB (185386 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32b96b50db4e43f087ae9c3c2b12efb6bc42f1c3d58b8769dfa0b2883411ab33`  
		Last Modified: Mon, 22 Jul 2024 23:04:21 GMT  
		Size: 8.5 KB (8454 bytes)  
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
