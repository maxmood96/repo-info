## `amazoncorretto:11-alpine3.23-jdk`

```console
$ docker pull amazoncorretto@sha256:cf46c576107dcb18ae0b07124ff51c0fc1e077d1724f85190265edfa0df91529
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2d9bc83ceabbb6f387e454d74ff52345acc12a17cd88a9f16f98078beaca6d70
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **147.5 MB (147531766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dc7f50a70e447bd97a2cbc27f54534d0225716c8eae1f0cfe421666227eeff9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:53:46 GMT
ARG version=11.0.31.11.1
# Mon, 22 Jun 2026 19:53:46 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:53:46 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:53:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:53:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a1746604200f5cdfb8a9b9589d3e328cba7b98a569ef703ac91c5788eacd7a`  
		Last Modified: Mon, 22 Jun 2026 19:54:03 GMT  
		Size: 143.7 MB (143687345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aaa14cd6f71188a8966954ba33ac1d81a4bb158d7d958b7a3c7117f1a6d63677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.0 KB (597030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf634c8ba5633b626b8013393069ea1674a808c65104aee0ff0341ba7c41a4c4`

```dockerfile
```

-	Layers:
	-	`sha256:d58b7c41f0e52ccf31eaf0e2ab0b1382a251b1325ba2fb97318c669ad9e452ce`  
		Last Modified: Mon, 22 Jun 2026 19:53:59 GMT  
		Size: 587.7 KB (587651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58db1c9dfe1b046dacf63bfb8088d5f8ea02362d78737e1ba11fb9fd14c91ed5`  
		Last Modified: Mon, 22 Jun 2026 19:54:00 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:646e35ebf1a2772033ff71e0104c01744b9456cfd2ffdc126a52f914ee565217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.1 MB (146144200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ac74ae16fe0f9209e73720a8c159b9e0e3b1e18d37c9cdc2e0fe63be55d37f4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:28 GMT
ARG version=11.0.31.11.1
# Mon, 22 Jun 2026 19:55:28 GMT
# ARGS: version=11.0.31.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:55:28 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:55:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8683304bda8ce560f285b09076d98d5f0e700914aa0c678dcf8e2490693ebd7`  
		Last Modified: Mon, 22 Jun 2026 19:56:01 GMT  
		Size: 142.0 MB (141962340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:28d49ec9206337130027b52012e319a0e67757a5835a210020f573236bcc154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **596.5 KB (596540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:939ef245b7d4e97a335a18a27eeb78dfd41db8a2f31bd84e9f26935f2f978e5b`

```dockerfile
```

-	Layers:
	-	`sha256:94ec7207188d96f6ff64f889c957aa9b62ec6db7e331851ee58b17bd8084d9d0`  
		Last Modified: Mon, 22 Jun 2026 19:55:44 GMT  
		Size: 587.1 KB (587057 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a3e40d326eb2ff1dd4479de0b14f71e7af56c02f1cef19a6516a3fef55f1ac4`  
		Last Modified: Mon, 22 Jun 2026 19:55:43 GMT  
		Size: 9.5 KB (9483 bytes)  
		MIME: application/vnd.in-toto+json
