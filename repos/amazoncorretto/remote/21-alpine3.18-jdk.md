## `amazoncorretto:21-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:1896cab5e9b193771659ed974d6d0e3151ce4b501fb970274b32086bf9f0bde0
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
$ docker pull amazoncorretto@sha256:25a61be200f4a1bda422f030d357c79b1e69063bdd9e3aafd5e1f0ceb8b31326
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.8 MB (160819618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8857f57b5532c4a2ca5b8b8bc25c0607f556c264ce33ca1af5307250abb26979`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:41 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Thu, 20 Jun 2024 17:40:42 GMT
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
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3a08b2c964d3b0a139f75671e05d36fefe3932b0897835cb628e78ca7b62739`  
		Last Modified: Thu, 18 Jul 2024 01:23:08 GMT  
		Size: 157.5 MB (157481669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b208d588ea7ef557c9cd1a70de242809542aaee0cee63567a31d1fc1c4d78523
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17c1dc9da952f2cc75dcd992421897318ae537bb0631471614da86b169bed512`

```dockerfile
```

-	Layers:
	-	`sha256:8a7585c73f48d4431f7cbb5b2e50cf4aabd41703768091a75601166f6c0b4edc`  
		Last Modified: Thu, 18 Jul 2024 01:23:04 GMT  
		Size: 380.1 KB (380071 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8c6006a890f3d46e348e18c1627e67f69069e2675f1db96802ec56c1f92487`  
		Last Modified: Thu, 18 Jul 2024 01:23:04 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
