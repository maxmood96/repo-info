## `amazoncorretto:24-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:d1d990bdc63a9938500f316d4ff4e56dd666b9e83f30bd4ed690a6506e96ac7c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:038c5512de5d341dc268a76626be72d61cd1684adaf77b7167df56632be52581
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.4 MB (180397735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:928c4fc1f21f5f5f579d4ecccce7c4f20961c6742d4fbcf788a3853735026c69`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b1e1eaf0f10836f476720a5a9ea386ee5efca91a5786261a51a8b01e100ec5`  
		Last Modified: Thu, 09 Oct 2025 09:10:42 GMT  
		Size: 176.8 MB (176770679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f01dd399a92a87450dd55a83e33ff5d12a42f5fa214d96b26644f18e6e15a826
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7363fd7de319816bb82010c11e2df9175c5ad9bbb5357fc9c29baefb64566ca5`

```dockerfile
```

-	Layers:
	-	`sha256:8d5090739d139672816d1175713be5d235a156e0f4474381888386a46e0c4853`  
		Last Modified: Thu, 09 Oct 2025 00:51:02 GMT  
		Size: 387.1 KB (387070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:399bc6c7b9d1122f6ec9c32c1e050a7b573d4d407dcdbfe5ccb1aa5ce513fe0a`  
		Last Modified: Thu, 09 Oct 2025 00:51:03 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f4f8a11a817c5347fc126f6170815990b4a8b093b244fd65570e27c4b60f7c91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.6 MB (178607588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932d821e23d747310d24770bb546c9a250a0af0cc035ed1050a1f340f3030ace`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=24.0.2.12.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3059b58ec33f2cd4084d1aba9d033196d7781990d5bdec88de14d41e1ea7a9c`  
		Last Modified: Fri, 10 Oct 2025 20:49:21 GMT  
		Size: 174.5 MB (174518211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7975067a34b4f5c52d221bbaaa2ce452a8f1c695efc7f606e53afcb264e0417b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 KB (396005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf0224eeb25225acfb9f2a5914f0f0a3b7c5cfcd18f4da449bc45a61c16e35e0`

```dockerfile
```

-	Layers:
	-	`sha256:efc150b1b94dd02e3a2192b0f1c088333c36c0acc1ab23a97fe293948af46717`  
		Last Modified: Thu, 09 Oct 2025 00:51:07 GMT  
		Size: 386.5 KB (386486 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:acf7945fcdd6f2f608b5d74de6adef7f39905d08c9f60acc71896ba1c2b8e9da`  
		Last Modified: Thu, 09 Oct 2025 00:51:08 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
