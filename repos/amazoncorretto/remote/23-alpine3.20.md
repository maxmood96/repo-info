## `amazoncorretto:23-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:c762b2f4eb64e378d61eb6c3f33949d0ec684e257c3aca3ddb9435b908e31ff2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8d036232aca562d17233763ee66128721f9f7f74fa774a4c80bd7cf99b99d8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170282626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f736d81775e5d83d76b91706dc12406318f23412ebfa230b5b8a80305720de6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25cb0e56189aec6fd6d729ea804a95d0a679874f87742459c5111e9c029166d9`  
		Last Modified: Tue, 12 Nov 2024 02:37:43 GMT  
		Size: 166.7 MB (166658722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a00b1de21cdb5df7e65ad7041a6c22110a20c4cfb575bfe7574f5a4005be32f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.2 KB (391160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96022e6e3068a954f8da5db95fe3dba5383c9bf21dc353297feaf52b21349130`

```dockerfile
```

-	Layers:
	-	`sha256:a3c08fda70216523d2c6c6db4993f1ce8ae028a8924212d4b2f8484c2f209be4`  
		Size: 380.4 KB (380440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb40c4fc458997dcb27a4b555106ba0380844232c6d8fec5474c85627619f12`  
		Last Modified: Tue, 12 Nov 2024 02:37:40 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fa493b893e361f55aa0d0c6e91481fd54d5c1b38338e4948583d313e2279dbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168439982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5157a7c1d5b54faffe67fe0b26f319d054ec9605d371581ced2ccfd6be147f20`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef1413bef328b2e591c8275ac22907ac0cec7bff979b30006b16e8a64026a130`  
		Last Modified: Wed, 13 Nov 2024 07:54:46 GMT  
		Size: 164.4 MB (164352256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ab9ba1b53436e2cc5921b2001530e4bee15329c7dbd5c4833779f18d9af7532b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.1 KB (390137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cb54260ea1b34e617bced6fcd63d06524a4b38452fcbd60b13473fec15be611`

```dockerfile
```

-	Layers:
	-	`sha256:fc9479b61017acf02829141705a9465e1fb159c01b36ef141e10c9507d7be8b7`  
		Last Modified: Wed, 13 Nov 2024 07:54:42 GMT  
		Size: 379.3 KB (379265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f91a1c508498455801c403cb5136740168992a005faba92ee0044248888018`  
		Last Modified: Wed, 13 Nov 2024 07:54:42 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
