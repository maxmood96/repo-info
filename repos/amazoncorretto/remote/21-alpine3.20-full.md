## `amazoncorretto:21-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:d871cbc6a783d25d3189df073eab66fbadce11074fd9ddbc6f0a9908c1c8c52b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8834a26cb6a60d6ebb41547c3678797f61bd2ba73a8914047fa1f1458814f248
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.2 MB (165190642 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c14152ac03a3a99e08452349e0956e5d1392080c4995b6101b364e4a883afd0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a7b4dd858ed216d9324379be60f0df9085ad0a98f7fbfcfe2016c2b4f86e89`  
		Last Modified: Wed, 22 Oct 2025 01:05:16 GMT  
		Size: 161.6 MB (161563586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:23526f21e1178d48651384edbf8177f26fc4c77f5d7f96df88b973de1248ffff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.0 KB (589968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ab63343d5cb545cdbef1e9341e02cd1273f8ff20a3b6b6ec1c9cc754fdbac73`

```dockerfile
```

-	Layers:
	-	`sha256:39f530c9897dff544e407a65895f13c6d82e3bd4f2c99df1c1deca6deb7416c9`  
		Last Modified: Wed, 22 Oct 2025 00:52:25 GMT  
		Size: 580.6 KB (580553 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:061f785d2f7415e62a23e3dd98cd2024a6a4489dc819fa494856e7d828676e38`  
		Last Modified: Wed, 22 Oct 2025 00:52:26 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:cdb6e1bf396e343b22d3ba6f5e9366600f98b2d37077720578ad365891288fbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.7 MB (163687940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87b3c1c8704b69651bcbb5117ad1b42665987c4f5cdf1f82a2419dc084ecfbe7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1bf608d20745f6302937a16f21128b734575f36e91be3371dde73bfbbd20658`  
		Last Modified: Wed, 22 Oct 2025 04:30:22 GMT  
		Size: 159.6 MB (159598563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5c941e3054fe3da168dd49facd3da59844095a031ab5d09b293ed773196e16cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.5 KB (589491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a8f361c427cbf8d1b5b189a7f66f4556edf66dc756894e62b6c3f622f7a96b6`

```dockerfile
```

-	Layers:
	-	`sha256:799db3864159334148cbd578087a1ebaa9c4cacd34da218fab83787ab23beb8b`  
		Last Modified: Wed, 22 Oct 2025 00:52:30 GMT  
		Size: 580.0 KB (579972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7941d8b6f974b4fe28f92ac72b8e8a9f8d4e763203ab1382d2427f48295c3a4`  
		Last Modified: Wed, 22 Oct 2025 00:52:30 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
