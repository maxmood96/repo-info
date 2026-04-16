## `amazoncorretto:17-alpine-full`

```console
$ docker pull amazoncorretto@sha256:4b1eb8f177547a180d8e8c34ca4f90aa41d0980a77bc5e9dbf88355b9e3b6c77
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1824d434b36b809a0809d37c13a9a7ce01c6506979fb0bac169cd6806dfff509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152232050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af7eed2b9da639da2b07acb33e676b7887efb6798e32715913e039e885fcd80c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:28 GMT
ARG version=17.0.18.9.1
# Wed, 15 Apr 2026 20:24:28 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:24:28 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:24:28 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:24:28 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b0f64022b5c0e495d4201eedc4a15decc1b2128f49dcc9528d6dd6880b56a11`  
		Last Modified: Wed, 15 Apr 2026 20:24:46 GMT  
		Size: 148.4 MB (148367861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a02b2ef803d7ea3820e34b291abd2aa6a1eac88c99d6accbe2256ee4f937f0ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.8 KB (593846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ec172d1539d2af257936eb5ee1b9a9a8e2522c48f2866e6c3946788eab4953c`

```dockerfile
```

-	Layers:
	-	`sha256:5c5244afc5d0ce4d98250aeb78edf1c7a8881455405f1542f65d6b321720479d`  
		Last Modified: Wed, 15 Apr 2026 20:24:42 GMT  
		Size: 583.2 KB (583165 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87ce5e9d6aa49e6708caaae7f5495cc8de70ab068ee32fc2c9a8f451eced1ad6`  
		Last Modified: Wed, 15 Apr 2026 20:24:42 GMT  
		Size: 10.7 KB (10681 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c3e432971f675af7fea7b2f0e5387dddc97cdfc5ca0f7d0002008d9620cf7b78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150912290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5aadcc43b12c16764266611d50c3f86d032ddc5049165681acfc9f304b8dd31`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:44 GMT
ARG version=17.0.18.9.1
# Wed, 15 Apr 2026 20:23:44 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:44 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 15 Apr 2026 20:23:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d75bb72db3171986e40d7dd9f16be2f3fb3e3be9716e853c161d652ac946252`  
		Last Modified: Wed, 15 Apr 2026 20:24:03 GMT  
		Size: 146.7 MB (146712420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b9a50ef016e9cdb8741c105ed799a3b9e622b9ebbaa9689f27999a42235f3fe4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.8 KB (592816 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55bed77dc1a387c299f88773549f028655fc42ffaa4cc4620013741bec29c12b`

```dockerfile
```

-	Layers:
	-	`sha256:4896a8cc5150c4c6a86f2e4ab1ba8202eb7ed8ecfa8b357cd651758c23e1db59`  
		Last Modified: Wed, 15 Apr 2026 20:23:59 GMT  
		Size: 582.0 KB (581982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:65a4d21d73050a1ea122c709501d801f285fcf70622b42a0f684754bbfebfc76`  
		Last Modified: Wed, 15 Apr 2026 20:23:59 GMT  
		Size: 10.8 KB (10834 bytes)  
		MIME: application/vnd.in-toto+json
