## `amazoncorretto:22-alpine`

```console
$ docker pull amazoncorretto@sha256:c6a05b68069958f5051cc39c7c3f0fd745cb260b8d884bd7bcfffa51f0bd5fdd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:187f6e4c856b9da5911da6c46082e318f08a440b3c32442d7656164a07f2c7d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.2 MB (161219156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec289d726043bffa6e0b66d8b521e17dc0aa7a405d3803e9261d4f18fa6ff1b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:c41d1e65b5bf591b976639a49928e6cd77170ac5a4b84166f976de9c24936c9e`  
		Last Modified: Mon, 22 Jul 2024 23:06:54 GMT  
		Size: 157.6 MB (157596264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3b178ddd8eff3d5648d5b2919680669203fc47512b972cd23c6dcbf30903777e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94c77abd36a80f250fba27f94995cc12ee1df4f431f597b399deb66ed40ca1bf`

```dockerfile
```

-	Layers:
	-	`sha256:3fd82e90ad147ab85c9939f6c71b65defa37fa13aa9275d8d03b92c07b1945e5`  
		Last Modified: Mon, 22 Jul 2024 23:06:50 GMT  
		Size: 379.0 KB (378977 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:293699d72a3e28affdcef2c302bf68a4f7e3b1708a1c045a9ebf2f967c4d572c`  
		Last Modified: Mon, 22 Jul 2024 23:06:50 GMT  
		Size: 10.5 KB (10474 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d835e68c4accc0cb8809ab3496a1abb184814b9225187c806f82657f75c6b919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159280830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fb271c7b69e49ed895b4065dd60201da1c658ba7db1fb1391d20cacf6711a49`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:5893b25a591ff47218e93b92f9fc1ff73ccd174b6e29550140ae40f4b8c6a93a`  
		Last Modified: Wed, 24 Jul 2024 10:48:47 GMT  
		Size: 155.2 MB (155193896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5cba8ce9c0ae790657dd5439d823eb9c02627e6a2ec19711b418cd0845579455
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebb3d90184be45edf159b910f8b2dcc16a7a2a510e1ebf5f9ba5fe83078e63c`

```dockerfile
```

-	Layers:
	-	`sha256:4f8f9255456c40ccf099f26f05a2522aa6042629956152d91aa817fcca2ea5ce`  
		Last Modified: Wed, 24 Jul 2024 10:48:44 GMT  
		Size: 377.8 KB (377802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4970d5896f1f03a96bdb09c4433ca744a4c87797a719334d7907ca88082997ce`  
		Last Modified: Wed, 24 Jul 2024 10:48:44 GMT  
		Size: 10.8 KB (10823 bytes)  
		MIME: application/vnd.in-toto+json
