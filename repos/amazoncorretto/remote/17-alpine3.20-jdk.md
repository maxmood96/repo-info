## `amazoncorretto:17-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:86f063f2301ecea0ec8395c2ab0412921929b97706cec8972837d60494c6ee0c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:38e25e5bb07949dbe399fe842d2c736d60b63a95fd6bde2b8a6c38f1b8ad1b52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.6 MB (149640120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1938c57998adf3ec68b62ee6ca8f43d151d1454af380e042e3e0f13ddc49e1fb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:3b646d0833eb63fc43b035e2301905349a3c03a65c260a6013d3a6236e8839b0`  
		Last Modified: Mon, 22 Jul 2024 23:05:01 GMT  
		Size: 146.0 MB (146017228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0dcb30f71af93f9313018640999d95e51f3e45d7ca4b1a85511ba8516fa9b61c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 KB (388316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a403455b32d85891854f9ff27397d9e381b4505c6f0f0473ca1a568ba8732698`

```dockerfile
```

-	Layers:
	-	`sha256:c34ab542ff102118addea5faee62e86fb01876d0a856d6ef8f0d3977038fdfbe`  
		Last Modified: Mon, 22 Jul 2024 23:04:57 GMT  
		Size: 377.8 KB (377836 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f220832ad81cbd7b230605b223d03f1face243f47f89d7eda86e0a973bd94be`  
		Last Modified: Mon, 22 Jul 2024 23:04:57 GMT  
		Size: 10.5 KB (10480 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c71c2b78b41e1b4fe1aab4c4f8c830f33d0d75ca35f8d0a9bef85d32bf202e70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148438274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c59aaf962f12e6caef0b402d35e31c4ed624545cd8569894351b25123d326ad`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=17.0.12.7.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=17.0.12.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:10c1e7c2f51d2442529d657bb6528774bb10bbadeb668b0deb30d9277fea1793`  
		Last Modified: Thu, 18 Jul 2024 01:18:05 GMT  
		Size: 144.3 MB (144349474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:77f208c29c5dec58b9d57bf1e5c11500719e77290ef6de851b7a7d7f9d6a5b21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.1 KB (388130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fa70e486a122cb03861d9577ca1810b3eca87abe9b1681ca5368f52e49ca7ce`

```dockerfile
```

-	Layers:
	-	`sha256:4a51b4973fe22d474704da001f028bdd06074970daaee0b0d3b9ddc48cabe928`  
		Last Modified: Thu, 18 Jul 2024 01:18:01 GMT  
		Size: 377.3 KB (377302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d95e2b80a810d767ee9a0759820ea5ee5cf78b5a33f450a2014c8c213db3c771`  
		Last Modified: Thu, 18 Jul 2024 01:18:01 GMT  
		Size: 10.8 KB (10828 bytes)  
		MIME: application/vnd.in-toto+json
