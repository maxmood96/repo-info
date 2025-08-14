## `amazoncorretto:8u462-alpine3.21-jre`

```console
$ docker pull amazoncorretto@sha256:7c17ef2e66632913058b392e24beb7a9359d6bb512dbb0fe3ad76fd102cd6618
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-alpine3.21-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:01c2a9b3eeea82d85ca6a95b16c1700d2eed34cae50d8ba4e539fc7d14b4b193
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45369195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ccab3d07162d7e433ffa44be3164e475d5be3e5f5f19817c1f8974471577cbe`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:0368fd46e3c6d237d81390ff086f93aee216df5cfa814041a491453fb0932a12`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3637570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64091b8355c56af0201e8df07528be88bc281bd9c5e6a13b19c51155f382c69c`  
		Last Modified: Wed, 16 Jul 2025 20:25:00 GMT  
		Size: 41.7 MB (41731625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c29dc95088feb7ca77f448f301128f3ae1db4c5eab11155f0924c5f51fd51a65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 KB (198616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f309b917718281e8dba11e8884a90b23a10ea34661871901208bf382b0bc1a0`

```dockerfile
```

-	Layers:
	-	`sha256:5ee60f75009772f74a7125f976eee893460f358f8ff0c1906f670e5698eebfc8`  
		Last Modified: Wed, 16 Jul 2025 21:51:27 GMT  
		Size: 189.3 KB (189257 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bcec093005c478ef054f1be5cc126f6ce369463621d692d0bb6fd1737d2b48a`  
		Last Modified: Wed, 16 Jul 2025 21:51:27 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-alpine3.21-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:477a9a4555377f73e2a7beb723fe1d9b18f3e05809a2d9c9b78d442a586cea05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45423904 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:694098129d296784c9c255dd8f35169ab88152f3ffec93e5bf62849b86e0a29b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:30:48 GMT
ADD alpine-minirootfs-3.21.4-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:30:48 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=8.462.08.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:d06c6b665c9b4c183a2e300b290a6b4b7db03f803122fe93d91e9178f425e488`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 4.0 MB (3986937 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83100f3ab68c44746c797f29c16bdb1fe0a718edfa100c45f170ebb92b5c374f`  
		Last Modified: Thu, 17 Jul 2025 01:48:25 GMT  
		Size: 41.4 MB (41436967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.21-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:21675ae8fd11f5b49bbe604ce9d11dc81ec9bd9f4660abe7f523e64684d7fe4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.9 KB (198851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83243655786db520b4305d71b6cc119a9e1a448dc080365c225bc8bd3cb3e6f0`

```dockerfile
```

-	Layers:
	-	`sha256:ef775ab2d1d7ed5405da9dc610bef17f77e69f2be14938ce486feee22f9ede68`  
		Last Modified: Thu, 17 Jul 2025 03:51:20 GMT  
		Size: 189.4 KB (189389 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c4cbbd712a897e18114365a89bad571cd1d37ded5f841c5c914de89fbb369bf2`  
		Last Modified: Thu, 17 Jul 2025 03:51:21 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
