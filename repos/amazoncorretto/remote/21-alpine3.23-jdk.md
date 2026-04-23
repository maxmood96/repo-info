## `amazoncorretto:21-alpine3.23-jdk`

```console
$ docker pull amazoncorretto@sha256:a1734d6cd1e2a0483870d2144ec012dabf91db80172611d92b7ee4f0d8ed84d6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:779289d94de53215a0197db9d09db1e67a3bb9aac85c52199448b23c5d42f98b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.7 MB (165677350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f20a9a6ac9fcbdc16eafaeb58c431802ba39f7eff84f785a9ab3ac4d3562683`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:52 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:52 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:52 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248b05a9ca5f91c177d0decf2d392d42cc189cd2cf569e6cdb0fd2b734d669bb`  
		Last Modified: Wed, 22 Apr 2026 21:35:12 GMT  
		Size: 161.8 MB (161813161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9bed266a69a82394ac214f12a6c978421a30d831b26961410579b12861dcb151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 KB (594401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8aa574b1a7af899491c465a9c5f13ffd969747aaa38b2bcbd26232238576c5a`

```dockerfile
```

-	Layers:
	-	`sha256:4a44ce5000e17c716df44ebf41cd667c1f4a9f6c323be1c58d8e0a418ba05f7a`  
		Last Modified: Wed, 22 Apr 2026 21:35:07 GMT  
		Size: 583.7 KB (583714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cec7735de6ff306d4335282fd7b991c93e192e59d321b98be9070c475464b4dd`  
		Last Modified: Wed, 22 Apr 2026 21:35:06 GMT  
		Size: 10.7 KB (10687 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2348083cc62e9d1e8ffb0dc2a887b9a2a3ba2e21cf963ac8e6fc299718a14374
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.0 MB (164028372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41875374def66db1723ecccc408873d600a948be7ea370be08be0de399794ba0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:45 GMT
ARG version=21.0.11.10.1
# Wed, 22 Apr 2026 21:34:45 GMT
# ARGS: version=21.0.11.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:45 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ecb8ee1bb766b7846294cccb87c572391bd352b362a7867597720dd8b7df36`  
		Last Modified: Wed, 22 Apr 2026 21:35:04 GMT  
		Size: 159.8 MB (159828502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9c90c174ae165e5dc1d5abf8f5dbf2caa371ee5898d6d15e3a764f6be8d9b97b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.4 KB (593370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1407ee0a26512356c1a63489cba5d332faa47283c4b1caae03e5f060f7835316`

```dockerfile
```

-	Layers:
	-	`sha256:3fcb8072d221bb5a9fbbbaf710492aded90c3443081e918b30f75d4b77b26693`  
		Last Modified: Wed, 22 Apr 2026 21:35:01 GMT  
		Size: 582.5 KB (582531 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f11079716194f09c5952633ad188ffd04247cc8f6f98bcab5e17a5ed35f50a57`  
		Last Modified: Wed, 22 Apr 2026 21:35:01 GMT  
		Size: 10.8 KB (10839 bytes)  
		MIME: application/vnd.in-toto+json
