## `amazoncorretto:8-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:dd70ee2ebf5789813f4749785a5408fc886d013144028106d6135e57d8d60d95
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7bec2d4612984047095b02c0e6b1b58797bb826966d8156f044911e67a2f7d31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103747604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbd08ccfc16b37390417067ddd3224f51fd2c84256d3087b1ed6bc03cf08a840`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 20:16:57 GMT
ADD file:33ebe56b967747a97dcec01bc2559962bee8823686c9739d26be060381bbb3ca in / 
# Thu, 20 Jun 2024 20:16:58 GMT
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
	-	`sha256:ec99f8b99825a742d50fb3ce173d291378a46ab54b8ef7dd75e5654e2a296e99`  
		Last Modified: Thu, 20 Jun 2024 20:17:32 GMT  
		Size: 3.6 MB (3623844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0af0822a9eff913d8e6d6d0c141413e4b29a3276622313c5de398fe19aaae19`  
		Last Modified: Thu, 18 Jul 2024 00:55:40 GMT  
		Size: 100.1 MB (100123760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4cd30bc485e774c8dd310e18b6fb1f0da9d3d92420849d7eb95d7cd3a835f9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **253.2 KB (253249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:475e7004811319e1cd5e36de054662b3e767a07595f4818275e4d5d3574dfc72`

```dockerfile
```

-	Layers:
	-	`sha256:150ad7c961f7b2da11ef2da2c06a2109a23b70d05a7c9ec1a2db61c73db6631f`  
		Last Modified: Thu, 18 Jul 2024 00:55:38 GMT  
		Size: 242.8 KB (242798 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:66d7d3ecbd7f59155c74d5b3769969e5bbab2ba5dc52b4e18999cc633d864ed8`  
		Last Modified: Thu, 18 Jul 2024 00:55:38 GMT  
		Size: 10.5 KB (10451 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-full` - linux; arm64 variant v8

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

### `amazoncorretto:8-alpine3.20-full` - unknown; unknown

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
