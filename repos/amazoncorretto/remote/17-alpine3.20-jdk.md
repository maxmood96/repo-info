## `amazoncorretto:17-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:b6e5aab53c360dd5f9843b18b397dee2ceed3211ac9be6cf36a51606d6ec015e
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
$ docker pull amazoncorretto@sha256:baa09949eec16a99442801970fbe453bca7a324bf5b207e324eca404c50ed388
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.4 MB (148436439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75759457a241e12df21d7bdf1684682073290864290c3f9385e112e3cdc100a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
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
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35cc4d59d1ea7d74f5a2a736f489f2ba657132f8814720d95e959f98ff12fc2b`  
		Last Modified: Wed, 24 Jul 2024 10:44:16 GMT  
		Size: 144.3 MB (144349505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d7b13c1021210f34c39386bbcbb7dade0f8f9da6a85aff8e5139da62dd77d7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.1 KB (388130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca83266e5be0f0e6b3e58ed62036ab2f4e0682e11daa85746c433560e53c352e`

```dockerfile
```

-	Layers:
	-	`sha256:43e7ece2ddbdbbbe03518cbd7d3c5166d27e791a25dc1759a0fdfc7b3761c371`  
		Last Modified: Wed, 24 Jul 2024 10:44:12 GMT  
		Size: 377.3 KB (377302 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e6a11cbd49caa6e8aea86b1f709e0ba793ddf62f60e29edc691e267c5228b67`  
		Last Modified: Wed, 24 Jul 2024 10:44:12 GMT  
		Size: 10.8 KB (10828 bytes)  
		MIME: application/vnd.in-toto+json
