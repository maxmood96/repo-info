## `amazoncorretto:8u432-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:ea7b71ba85e699f49aadc99cd94bde718dbebb1426785352de15ff8b57d2e13f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2245b8edbf3877f9f33467963b5c4674ec47c83a0d43b3c5bc7440c86df89144
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45072286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa12e385bfd54f883c5644588bf3b8461b4f3a54200c11fd25949febba948e88`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93fbb9a965d3205e852905aac174b5034d21ce0ee781f5b26488ea9edde1d75c`  
		Last Modified: Tue, 12 Nov 2024 02:11:40 GMT  
		Size: 41.7 MB (41655885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fba302d3365f7fd6fc09075ea896193bb7ff4c43612b3fcbe5df0c3b64333c95
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8fba0ad168bba03a7921159d87df15688ddc074ebdee234fa5127ed8149d162`

```dockerfile
```

-	Layers:
	-	`sha256:a79f0bfcea4b0c166eabe5364e7d6102ebb63f0b34a27f222248687239d5aa27`  
		Size: 184.9 KB (184864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d45459153e6edc35892ad380ae114b40158b0421498aea024d22237f3475d2c7`  
		Last Modified: Tue, 12 Nov 2024 02:11:40 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b5bc9ab13e9209ef8b70d316c0f6f4658c7c17953a809db23328cdaabf16931b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44698762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c25aca705baf2bcb2e40846947c765501a9f03d431f4d53bfd77905d41e7ae9c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98eaeb09b73e24eab789d529f6ece567025646e70aae1638a07b460293e56c9f`  
		Last Modified: Tue, 12 Nov 2024 11:03:48 GMT  
		Size: 41.4 MB (41358311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fa0ccaa4f65197684d99dfec6556125fac6cdcb144e6c4368b6f6083f79d1664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.8 KB (193751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e33fe248715b2fdfb38f19ffaded052e4c17611d41b5e11290807b6a80f0e29`

```dockerfile
```

-	Layers:
	-	`sha256:2c5d2b0afb80aa3d011412e390f96a8c3995b394413ce81c677fb881213ff114`  
		Size: 185.0 KB (184972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f66e84645c8372df2b17acece2769e7d2a480dfba5a56accc0fd9f87f5efdf2c`  
		Last Modified: Tue, 12 Nov 2024 11:03:47 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
