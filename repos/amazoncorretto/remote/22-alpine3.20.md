## `amazoncorretto:22-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:95e7b8f5b63a195e0e50192aaa2b9ff6a0e8e49c8214e32568942335693e18b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.20` - linux; amd64

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

### `amazoncorretto:22-alpine3.20` - unknown; unknown

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

### `amazoncorretto:22-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:50d96af1da008ae08cdd4cb36476d59ca647f151c9adbdf428a6801658281559
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.3 MB (159282692 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598acf98423824ee77d8087c06086697791128fedeab71e4f57902317fa5b83f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:35 GMT
ADD file:033626ac44156f3d5800a602c46870486b1492b9ba26096eaa66cceb6fcead77 in / 
# Thu, 20 Jun 2024 17:40:35 GMT
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
	-	`sha256:a258b2a6b59a7aa244d8ceab095c7f8df726f27075a69fca7ad8490f3f63148a`  
		Last Modified: Thu, 20 Jun 2024 17:40:58 GMT  
		Size: 4.1 MB (4088800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0928dfd4eb881c902cc98e076f25b472614faa1a302120d50981b3628a023fce`  
		Last Modified: Thu, 18 Jul 2024 01:30:33 GMT  
		Size: 155.2 MB (155193892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e87c0e6777310d2d617ffa93192d847ab14a82edf042ff91e5e4b28230f44c81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df963dce18ac4ea49becad2928ca28a34d59ca3f30330aa768b73eff6d94d293`

```dockerfile
```

-	Layers:
	-	`sha256:e23b9fa34442c2e1350c67c327922105f62b8f929cc9b6e5e5474392382815b5`  
		Last Modified: Thu, 18 Jul 2024 01:30:29 GMT  
		Size: 377.8 KB (377802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eabc3bb935450583a4fd4d126d185bf5aad17881f263693a893f672693900e8d`  
		Last Modified: Thu, 18 Jul 2024 01:30:29 GMT  
		Size: 10.8 KB (10823 bytes)  
		MIME: application/vnd.in-toto+json
