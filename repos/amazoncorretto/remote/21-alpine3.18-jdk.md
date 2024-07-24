## `amazoncorretto:21-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:a770a392039c231d634aedccf0186bf8917ce6c358f5eae7ad6256d47d57d660
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2b9d84ecf890b88ad8214ffbb6c16ec24c93d8b9371075602a526d0d15e2bb32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.1 MB (163141319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3acb8a544abd023323c4cfea23c569fc5b409f1d1f55bcb4f0978e05368297c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:177f6609682a9c187a321ed27d7d200a5bb83e4fbdd2f95b7f8a8f6db266a0fe`  
		Last Modified: Mon, 22 Jul 2024 23:04:52 GMT  
		Size: 159.7 MB (159725679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:98cffd5c0d5c39cef973fcf5abfba7c384337f91e20d43c9911786acf041dbfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f0e24bbd791653774c72fa832525e07793a59dddd5682ceaef868c53cf7df1`

```dockerfile
```

-	Layers:
	-	`sha256:3b5631e4f4d1ee70ec673c1d5dbe4a52e8a3583df83b5cad483dbd920de72cbc`  
		Last Modified: Mon, 22 Jul 2024 23:04:50 GMT  
		Size: 380.7 KB (380653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f2ca18ef49771782a98ad6dedd10a0830f33d3ab37103eadab5205d9e26163c1`  
		Last Modified: Mon, 22 Jul 2024 23:04:50 GMT  
		Size: 9.2 KB (9169 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:46a8af65ece8242bf59689cb98bd3741b7966666570c4c2f5cc8b09f06a5fd17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160821232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91353168ef1892046823c91dfb0feaf76e731faede76cc69eae35931e453f29c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=21.0.4.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=21.0.4.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d903b89dfc956ea95140937deb6776267b91c4a720cae54ac4483107e32255a`  
		Last Modified: Wed, 24 Jul 2024 16:30:32 GMT  
		Size: 157.5 MB (157481738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:022ada68b9a1391977651d696586eaaf20ce8d0c65d020fc1289c865944dbc61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbf53c80dc56f9e39fe2943f34dbe7bcf575e76210a538b757cc83766b9ab917`

```dockerfile
```

-	Layers:
	-	`sha256:95e6bcc3b486e93600ed566de71b38d710005ad38ea32482822d2c55fb7cb1ca`  
		Last Modified: Wed, 24 Jul 2024 16:30:27 GMT  
		Size: 380.1 KB (380071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c497b555efc049b3f8551beb04b15d414b2dcc9fed4e20b5682c8fdcc72cf324`  
		Last Modified: Wed, 24 Jul 2024 16:30:27 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
