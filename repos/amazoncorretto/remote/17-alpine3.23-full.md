## `amazoncorretto:17-alpine3.23-full`

```console
$ docker pull amazoncorretto@sha256:bec4ef1904116e471fed3eeba0069ebb012188be1eb904f3a17eea2fcf3a7dda
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.23-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c55787fd16ab780f64a612a701e762b437029aa40501db821a2aa427718f64bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152427978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46f072d48a70eddf2d4b830ae10a1bed6b7181908d16661a96f79fb7a957f0b6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:09 GMT
ADD alpine-minirootfs-3.23.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:09 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:02 GMT
ARG version=17.0.19.10.1
# Mon, 22 Jun 2026 19:54:02 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:54:02 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:54:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e6f31ffc071e5560b82a8685fba8214954e5721e3e49269d00958316edbe89fe`  
		Last Modified: Mon, 22 Jun 2026 12:03:33 GMT  
		Size: 3.8 MB (3844421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0943e9de0ebdb673c653ea170f5cd09c0dc2b64821e10b92450d4e67726e26ed`  
		Last Modified: Mon, 22 Jun 2026 19:54:20 GMT  
		Size: 148.6 MB (148583557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e658d7dabf41b4753d991500b4a60f7701063bc5d0629a75893e96bb43a8e747
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 KB (591882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78e8656e9f69ef84fb9b061ab85f320d489b6be4f18f1d8907e0c994bc2cf70`

```dockerfile
```

-	Layers:
	-	`sha256:3ecbf3cb49735dbe1b58d254a3eb9ec6a974628b3476f28937e4cc6821b303ba`  
		Last Modified: Mon, 22 Jun 2026 19:54:16 GMT  
		Size: 582.5 KB (582503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80689239b1e9ca4559a9b8a546508a11d089a5cfb00528e0c000eb0e6ccc3ecb`  
		Last Modified: Mon, 22 Jun 2026 19:54:16 GMT  
		Size: 9.4 KB (9379 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.23-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:101a9f23bea1779b6aef2cf7f1d5426c7efafe01a86b5759fbe7d804f65281c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151119691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2defaff87992c65722c141d1ce6a20f93f6c04b2f03642af85a4ce489195e96e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:19:57 GMT
ADD alpine-minirootfs-3.23.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:19:57 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:32 GMT
ARG version=17.0.19.10.1
# Mon, 22 Jun 2026 19:55:32 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:55:32 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:55:32 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:14a4754c352fba4c6c0da8e4f01bb990463c19f7ff63e090073c385bd2bc5046`  
		Last Modified: Mon, 22 Jun 2026 12:03:31 GMT  
		Size: 4.2 MB (4181860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea08fefc67f59a07f32d58b63229ec1324f79ab163d6c7c9b926b8e4f94db2ef`  
		Last Modified: Mon, 22 Jun 2026 19:55:51 GMT  
		Size: 146.9 MB (146937831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.23-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:311ebd0cc4f5cd71db76ff5d29a900d8e57734513afde178ec33ca69f2dde2ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.8 KB (590754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e58b8832392feb420e5c4b08c62d729410e982ec2b1a7667310d17bbdc02d13`

```dockerfile
```

-	Layers:
	-	`sha256:c047bf74944c0c320c963383b44c2a4cfc1e8b3beead539c441d38306a78cd68`  
		Last Modified: Mon, 22 Jun 2026 19:55:47 GMT  
		Size: 581.3 KB (581272 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bcda6cf4253d95cc5901fe5b3aa31cd209f1019123e7560d070bbf588e3e7670`  
		Last Modified: Mon, 22 Jun 2026 19:55:47 GMT  
		Size: 9.5 KB (9482 bytes)  
		MIME: application/vnd.in-toto+json
