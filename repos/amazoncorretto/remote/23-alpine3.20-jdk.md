## `amazoncorretto:23-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:081cc5e88bf6b6157b083beb3dfbb18a2c9bcf159a5cb4b76a1c797f0a2dc20a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.20-jdk` - linux; amd64

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

### `amazoncorretto:23-alpine3.20-jdk` - unknown; unknown

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
		Last Modified: Tue, 12 Nov 2024 02:37:40 GMT  
		Size: 380.4 KB (380440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bb40c4fc458997dcb27a4b555106ba0380844232c6d8fec5474c85627619f12`  
		Last Modified: Tue, 12 Nov 2024 02:37:40 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:696bb0383ecd9f82db2b5cb415d978c70eaa8f845358951a8e51cf7958943b59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168439867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b4c884bc36f5df12ac6b640c9f72e21d878b7a4242544ac7a6e90af8f7a25d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec1ef0065c454eb9ae29eae0899d2f45f39e4e6a82929f0c88e27dd992af1ac`  
		Last Modified: Wed, 16 Oct 2024 18:46:10 GMT  
		Size: 164.4 MB (164352221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:79f9d55025d13ce62afbb9be0cfdd7d3148fc62820842493b4409cae8ce5c6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389829 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11fd82f35c7cfe1e47ec72f61252fe343f76bc2a206df2c837874d74c51d82ea`

```dockerfile
```

-	Layers:
	-	`sha256:c777163501bb7f393deae75b3789497da0095f3c75e3485a50e569840c2c3074`  
		Last Modified: Wed, 16 Oct 2024 18:46:07 GMT  
		Size: 379.2 KB (379172 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:623a1ebd53661d19bf8a5f789fa21e9e81861e33d2fabac06e24841e3c2e1bc7`  
		Last Modified: Wed, 16 Oct 2024 18:46:07 GMT  
		Size: 10.7 KB (10657 bytes)  
		MIME: application/vnd.in-toto+json
