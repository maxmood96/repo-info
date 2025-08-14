## `amazoncorretto:21-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:73e40088422c9ad0d4fb785efc2e04d7a98a544835f856bb6ad0426ebe157217
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d8414e4ba4bf7aac7675a5527afa99e6a13c1510f1976a31deb73eb9e1c60722
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162799576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d407af535344b9e79d87111a7917e8b1436daeb941f091103a6d11700dbfddb5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=21.0.8.9.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1747dece94917ce1b0256ecd60138ce4deaea1bd35dcb6b2e8afe697dd2f5b71`  
		Last Modified: Tue, 15 Jul 2025 18:59:51 GMT  
		Size: 3.4 MB (3415528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5aabc8d776c349fa6c7f373f3128492d36c4dd9f8adcf88cb4b2aad0a7d958b`  
		Last Modified: Wed, 16 Jul 2025 22:02:17 GMT  
		Size: 159.4 MB (159384048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eb0f13c7e035e8f9937d650430da39f6f340879c9d7d6f07389e6040a12bd9b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.8 KB (391797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ad23da3ede7a4a3bce606c6724213a6deb33f4c6ac1d188da400d3bffbfd817`

```dockerfile
```

-	Layers:
	-	`sha256:44b3ea45f79782065b8d35adbae9a344efc932feebe6bbddc7e493d80e3e6583`  
		Last Modified: Wed, 16 Jul 2025 21:49:50 GMT  
		Size: 382.4 KB (382383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2537b68d3456fc87522d181d251b878ca1454a5be084132c2506e19428104083`  
		Last Modified: Wed, 16 Jul 2025 21:49:50 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:925f76f463412ea8ecb04a7afb98411da8248e26aeb8d47649a7599ae9f6819a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.7 MB (160695095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1d8d8260ec93da6d89a62be7b9020e1aab31ccc28891aec354a667980b4c6c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=21.0.8.9.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=21.0.8.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:07e9a47f0c334cceba1b05e86ef0150c84564a9b9e9d4ae9dc9a5ebc85ef2b7c`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.4 MB (3353103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51bac8bdfdf4e07b2c2cedf1f51615406f5ff98cd228a4394041f4ce485b072b`  
		Last Modified: Thu, 17 Jul 2025 04:27:21 GMT  
		Size: 157.3 MB (157341992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c7465dabdf1a0d03237566cb54d804248bbd76fae421baf4cb66388aba61349c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.3 KB (391320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30935cf7e9e0e2a7e2dd76628dc20fd1fcbf6ac34a119fcc45d905fceeb390a5`

```dockerfile
```

-	Layers:
	-	`sha256:17e57873c21a632100269910a64767df7bbf65b5a417c71d2e7fbf6435a11900`  
		Last Modified: Thu, 17 Jul 2025 03:49:42 GMT  
		Size: 381.8 KB (381802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc202db532bb6c16b4a143f0d9121bd2bd3d12fc02c5705b1e38486beb5013f9`  
		Last Modified: Thu, 17 Jul 2025 03:49:42 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
