## `amazoncorretto:8u472-alpine3.22-jre`

```console
$ docker pull amazoncorretto@sha256:49802c682d9c4e5205170df985e395c67aadaf45071a1abdde9373a3681ce9a9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u472-alpine3.22-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:71069a44077b341fd5cb6c53c2737ae7f75cf6b4bfe3e1cda4834eaa970abe94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45534370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c8b9aee09f7aef613c1264a59a5b484a844c22c3daacdab0c21bdaa6cfca587`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83c28e49ada32dc2d63a0d20cf1818823ddc0617996c3c0a11b1b73947a85640`  
		Last Modified: Sun, 21 Dec 2025 01:38:40 GMT  
		Size: 41.7 MB (41731918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4932a3d2168d07cc4c0d4686d06e126b89bae043d680d718d1d702dfa71c9bc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.5 KB (198509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a42f4623091c3f93fee98d6568a99aa903ed8ec0f811a9f8c9690d76722b94e2`

```dockerfile
```

-	Layers:
	-	`sha256:a5d5dbd0944e085f533fae90fe7d3cfeca266c956a43be0c5dfd83dcc5c5b90e`  
		Last Modified: Tue, 21 Oct 2025 23:26:12 GMT  
		Size: 189.2 KB (189150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90989b963be00a93d1313bb90e26c1bb460445009fab2e4f0bc2194d5a61a9b3`  
		Last Modified: Tue, 21 Oct 2025 23:26:12 GMT  
		Size: 9.4 KB (9359 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u472-alpine3.22-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0f35a266568987fea66ddda059f1db9f2b7a24a3ffce6d4d110c11843b3ae146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45571560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f65df63e8de556d348ef6c36f88bba5b6ba1ba84f664427929a11bd5582af650`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e45f068f997b719864141a74c1692eccb62576064eba42ace80cc2f7b1b5ba9d`  
		Last Modified: Sun, 21 Dec 2025 19:01:18 GMT  
		Size: 41.4 MB (41433491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u472-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9fef6522c4af394e1086e74a182d1ea402734241891556b1831e2dd94562d864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.7 KB (198744 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b818320ff1142aa5a37613b2f9fe866b7bdb95a93628a87c9c80b74a2b3e44c4`

```dockerfile
```

-	Layers:
	-	`sha256:45dfcbd614ac3fc00ae24e17540bdd6e0a309b99947736e4f2522f4c8f97e973`  
		Last Modified: Tue, 21 Oct 2025 21:49:02 GMT  
		Size: 189.3 KB (189282 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feb5a1d05226a294d9749f78e15fafc48d19ec89f2969293ba971c81897bc157`  
		Last Modified: Mon, 22 Dec 2025 18:43:52 GMT  
		Size: 9.5 KB (9462 bytes)  
		MIME: application/vnd.in-toto+json
