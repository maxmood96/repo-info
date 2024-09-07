## `amazoncorretto:8u422-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:21708cbfaae811fbba487f2e8a689fe869c9c068d1eaee6c7418a27e06093f5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a0f4de17e7c50843155526926e39fbfac66a88f7b680b080caa719f921844dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45223463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925e8d26572d963d372a738be767819975116072f18e99142325d0161f6fb8c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd37011fa32788b39c2537127eb1bbcad8841d25b8c05537c3fbc875eb858049`  
		Last Modified: Fri, 06 Sep 2024 23:16:54 GMT  
		Size: 41.6 MB (41599656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8a80d3f6046caecd271084b3679e3fd64375b7b79f95534efe7385a891b713bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 KB (190925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98865fb75e9f4c9fd2d6f64d3f0d9790fb4d97cb6193818bb8ea26be867c14e5`

```dockerfile
```

-	Layers:
	-	`sha256:6bf24ddb58b81e597d969192d55c1e71664053ebe80e51285341d33c78bbd6e6`  
		Last Modified: Fri, 06 Sep 2024 23:16:53 GMT  
		Size: 181.8 KB (181811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170e4aac9c53b81e236f0f0877ae83e3a43f8f9b7830f3035cedd9c0a1d3e252`  
		Last Modified: Fri, 06 Sep 2024 23:16:53 GMT  
		Size: 9.1 KB (9114 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2b34b8c952e79cee499a6df9bd2d06ec69a758189a046cb29540646a04e10e36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45393685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29e2cd64e9b0213bf039c620c1ef5d3c70395b0087a4ef4b371e3588430a4b7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c70d30e562984c8880c3084742cfe272859b61e76abd182feefbc9840d4219ea`  
		Last Modified: Sat, 07 Sep 2024 12:08:17 GMT  
		Size: 41.3 MB (41306039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:da9cf218752e142c1b04a3be162626dfc6f1815fd1b97b9bb2d9987981a82576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 KB (191357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9231df3ff48eb4c054c58e1150a95065c4bc9186e401196b2abece388b4b4c0`

```dockerfile
```

-	Layers:
	-	`sha256:0ba48466fe879b12e9e779485994378595347dc4058ee8a1fd8462d9eb07fcf8`  
		Last Modified: Sat, 07 Sep 2024 12:08:16 GMT  
		Size: 181.9 KB (181943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8a478962ab6c0eb90495747c19d8f741766bc4b8b1cd58e24d0c1cb3dfa9761e`  
		Last Modified: Sat, 07 Sep 2024 12:08:16 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json
