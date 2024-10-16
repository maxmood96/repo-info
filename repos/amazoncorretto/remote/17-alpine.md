## `amazoncorretto:17-alpine`

```console
$ docker pull amazoncorretto@sha256:d7ac7ae33ee93cd88703611c59596e3e30c87c78eae2b1f8f2f81ed5c89b2cf3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:743417b059003f851a774dde936b4278fb06cbd5c1564b61d8b876bdae2b242b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149273091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ed11f56bcd0e986b910244273cac3ef0e75ecf8c575f170dc9d132da3fabcf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed661954c40c6df4b0773f9ed2104f02a996d32057e419223cc5c193a5446ab7`  
		Last Modified: Wed, 16 Oct 2024 17:57:29 GMT  
		Size: 145.6 MB (145649284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:48611b5235c5eb2ede85b23381dca84960c5f7bfc8cedd6a827e16d8e1c4d247
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.0 KB (389027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18bbac727207e397fe67300648f95ee025b1c3af8df817cc6852d8200c315e22`

```dockerfile
```

-	Layers:
	-	`sha256:0f540d78ca1e21f3f9fb6a58e7dd38e387cf3ff37369fa791c7a2a6728613652`  
		Last Modified: Wed, 16 Oct 2024 17:57:25 GMT  
		Size: 378.5 KB (378504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:091543e90c5b18360e51330d28dad696cefc4a76b8b7d93252d264b4b364e655`  
		Last Modified: Wed, 16 Oct 2024 17:57:25 GMT  
		Size: 10.5 KB (10523 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7399db70d7f7d048cd4af62a2cafe0307b94b87d64198afbd74dd4583549b9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.0 MB (148022279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0dbfe10caa20df3a2914790bff2eb45f0742f8b96ded255170681dc67c78419f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=17.0.13.11.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=17.0.13.11.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:644f628d973a703645cb2f2b4a6afac3e28403d169cf5a085cecafb375b39792`  
		Last Modified: Wed, 16 Oct 2024 18:30:37 GMT  
		Size: 143.9 MB (143934633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8b1ec0ce66f829f4f918559b61993a7bc330f5862830b44a6ca9ce30136fde60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.6 KB (388638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65a5b55ad8ea1bdd8640649b4d61d19b1c135ece9826d113ad16048fb0b76761`

```dockerfile
```

-	Layers:
	-	`sha256:63d7e6f9da3f97a7f9692cd66f74c83a3a594687dc29d27a9ee8c70378a61644`  
		Last Modified: Wed, 16 Oct 2024 18:30:33 GMT  
		Size: 378.0 KB (377970 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eff948cc16ecab608609c5fc039b48ba7250c59cf9e4344c7ed3d74ccd676b6f`  
		Last Modified: Wed, 16 Oct 2024 18:30:33 GMT  
		Size: 10.7 KB (10668 bytes)  
		MIME: application/vnd.in-toto+json
