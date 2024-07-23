## `amazoncorretto:8-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:24ffa822990a6ea9c1b5a4dd42ba4529470ca627944c7e10dd53f0a2ff219cce
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:98aeb096f72be43ad6fa5f0b2b84c74e62cffe235e9b68471f5b37da2850b499
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103746661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1044e2fb7a164f80f17a12f76b6aceba188e8ffbd8a7ed9abf8d695827d0c13`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fb0a7c7308fa1d64a08f426f3e117b9816f3f9bbb7ad79ab8fd2125255b0710`  
		Last Modified: Mon, 22 Jul 2024 23:04:30 GMT  
		Size: 100.1 MB (100123769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:723509ec87e9a12ba9f2e13447c3106b784ed6a933224963de03b00165a4a27a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 KB (253249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad50be7cd5675274e058024327a7cf1eea696808fbe5931e9643554ba057ec39`

```dockerfile
```

-	Layers:
	-	`sha256:e8f2b2485a7186816c0fa37f2d0a3abfa9f66f37ed993d88bc108ba361429a13`  
		Last Modified: Mon, 22 Jul 2024 23:04:28 GMT  
		Size: 242.8 KB (242798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2290d68a1c5fccdbf135ae82d7645eb25c3b1d0007e816f121de749aaef4bb26`  
		Last Modified: Mon, 22 Jul 2024 23:04:28 GMT  
		Size: 10.5 KB (10451 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6b6f0bbc4c28ae7c90e3d59910b4bd1815f92a02fdb6627cf66f7107c308db0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103923567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c48000858d13d3b4ada725e680f558969ca8c484ca5ab6c5289727ff27d9dec`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ebbcb4b6bb06838dea8c45abdcf25151f9504951a6faaccfc80967cce2f61c2`  
		Last Modified: Thu, 18 Jul 2024 01:01:24 GMT  
		Size: 99.8 MB (99834767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:640e5250f210d9eb910dc623105de4782a4f3d078c633952d2cc102fffd4e06e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.8 KB (253776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:042e438ea31c1f1977b1ca6f585221189d9f95aaf7916b14702055cf71e9be5b`

```dockerfile
```

-	Layers:
	-	`sha256:f2d9dbf18994fa2ed086f536da7fd50150e4e66b657cc0b12d5cc14e561c84c4`  
		Last Modified: Thu, 18 Jul 2024 01:01:22 GMT  
		Size: 243.0 KB (242978 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:773a219dd9926688876b5449e72146683c9e78dab9ce2125a2944480994462fb`  
		Last Modified: Thu, 18 Jul 2024 01:01:21 GMT  
		Size: 10.8 KB (10798 bytes)  
		MIME: application/vnd.in-toto+json
