## `amazoncorretto:25-alpine3.22-jdk`

```console
$ docker pull amazoncorretto@sha256:e3ffa47615ecf3ee5f97cad877b65666eb4340bbc07a853b223c1b17d26a89a3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.22-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:784402e849f51aa9e1f84878b857d702d860806e9fde407cac49b517b7202bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.8 MB (184788036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c4f9daea8e2eb81dbca5dae3738688cd1734efa2176335e42efedbdaf710482`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:21 GMT
ADD alpine-minirootfs-3.22.5-x86_64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:21 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:54:15 GMT
ARG version=25.0.3.9.1
# Mon, 22 Jun 2026 19:54:15 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:54:15 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:54:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:54:15 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f7ee36c9aa34bbb665f975c76e5c0d1607f0674b94c84cfb0061f87006ea5d10`  
		Last Modified: Mon, 22 Jun 2026 09:11:44 GMT  
		Size: 3.8 MB (3787595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8ad75c00d42d4e5911e027b46cd2c42103c09a1071260239c3ed7d1db45d114`  
		Last Modified: Mon, 22 Jun 2026 19:54:35 GMT  
		Size: 181.0 MB (181000441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1333383ecfea47bd5ee222d6ebd085341ab43f820ec53d251028f6341c331bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **602.2 KB (602155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c17ff228ed9240292dc990da0285d48c376073edcea34c203b899014f7a4e35`

```dockerfile
```

-	Layers:
	-	`sha256:907962424877795ca766648442e33c4d8e8040161cd9a534cc0c8d622c6a48a6`  
		Last Modified: Mon, 22 Jun 2026 19:54:31 GMT  
		Size: 592.8 KB (592784 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f944282c5cda6f56f0e9f5be5cc62fee3ca8d652a83cb88fc953fd8db5eaa386`  
		Last Modified: Mon, 22 Jun 2026 19:54:31 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.22-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:56809e6eca0116153422bd37412d6f70ac49469c6b1c74af91dbd1c63e0290b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.7 MB (182742258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9866412119118481faa5a4fcf8dbef46d7cf062a6145e292bc2e60c7a97bd11`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 22 Jun 2026 19:20:11 GMT
ADD alpine-minirootfs-3.22.5-aarch64.tar.gz / # buildkit
# Mon, 22 Jun 2026 19:20:11 GMT
CMD ["/bin/sh"]
# Mon, 22 Jun 2026 19:55:58 GMT
ARG version=25.0.3.9.1
# Mon, 22 Jun 2026 19:55:58 GMT
# ARGS: version=25.0.3.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Mon, 22 Jun 2026 19:55:58 GMT
ENV LANG=C.UTF-8
# Mon, 22 Jun 2026 19:55:58 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 22 Jun 2026 19:55:58 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:738128faa30f570583b0e57efd831e0e6a2a9aacf1be88c8f4c1ef8a5b7033cc`  
		Last Modified: Mon, 22 Jun 2026 09:11:35 GMT  
		Size: 4.1 MB (4120486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfdbbef87405cc68b73d0d6480690157f4e452e1bcc857581911fe2fd32c3e81`  
		Last Modified: Mon, 22 Jun 2026 19:56:36 GMT  
		Size: 178.6 MB (178621772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.22-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:edcebf7d62967518396e904fa693587b2758a9f7b1099ea7468fcfc964766d72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **601.7 KB (601675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fdf02c675b7477ffb90530a646daa07ba87fe7e158f2bbd9ce5ddfe65efeafa`

```dockerfile
```

-	Layers:
	-	`sha256:1fdc03ed6429cfa245f98ffa7f685d389cb3fa1594a03067a9e0fe721b3dde63`  
		Last Modified: Mon, 22 Jun 2026 19:56:18 GMT  
		Size: 592.2 KB (592200 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9d880281ac17140a3dda9daa6a724f5faee1cb8af864d47bb52b9d3106009c5`  
		Last Modified: Mon, 22 Jun 2026 19:56:19 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
