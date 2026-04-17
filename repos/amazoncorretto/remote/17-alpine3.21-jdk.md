## `amazoncorretto:17-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:cc134ad10160e51977310c925eaa98f09cedd7239929779899b3fafd0ad13ef9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bfba0df77a3c48fa8d3fe3d20847c878ca8f15e71570261d2a512e16f291f96c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (152013602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63b1cce39d9db65cad089406f263959fab6fd541845327e448af2c6c6ca12c6e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:43 GMT
ARG version=17.0.18.9.1
# Fri, 17 Apr 2026 00:22:43 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:43 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:22:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:338b45851fe8f0bfd2a01e6fb51ae353cc03241146899d278600a574fe06d9fa`  
		Last Modified: Fri, 17 Apr 2026 00:23:02 GMT  
		Size: 148.4 MB (148366727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:527275bdfe9c290c37268b1448d0fd748f01cdeb97661743c6c8942946fc0228
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.9 KB (595937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deec22e1d2e7d47c26d22e42597275d808fcb6dc2d2548770be95d24966f61de`

```dockerfile
```

-	Layers:
	-	`sha256:06526e48e2daafe2a3005a694d4a5c4731022b4daeea50a9a77bc5d379734da4`  
		Last Modified: Fri, 17 Apr 2026 00:22:58 GMT  
		Size: 586.6 KB (586563 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36607448ed2350d891237fbbc45ad4a322e22910da0e49ee8122f82a997ac23e`  
		Last Modified: Fri, 17 Apr 2026 00:22:58 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:c22e1bbdc2e76e21d5c4d18b1511bc570959f0419c9a14b0e8c40a81a525c9b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.7 MB (150697069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46448152b2b5258501aaeac3c2320f22b4100d04d494e19c651e28ef84ca8cbf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:46 GMT
ARG version=17.0.18.9.1
# Fri, 17 Apr 2026 00:24:46 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:24:46 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:24:46 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:24:46 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66e4bd68c36c553ad62843d3341b2fa352746e76885a8234012a02a173bde89a`  
		Last Modified: Fri, 17 Apr 2026 00:25:05 GMT  
		Size: 146.7 MB (146702604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5c8b776057d1d0256afa05da6bf29e3a9633003194957eb68899a4e8eb3f2793
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **595.5 KB (595459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07671de6c899baf8f5475bb5636d64470d34503009b62353ebe7e5a64fa3c0be`

```dockerfile
```

-	Layers:
	-	`sha256:ee44fa3a8e92e941f91165a1dfd991895a9b2f2b7097d9265079d42d4d5bd4cf`  
		Last Modified: Fri, 17 Apr 2026 00:25:01 GMT  
		Size: 586.0 KB (585982 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80f41ee5d463cda0c3f4fc4b73d72809902d266ba72d11bb9f8a7e702a89f9fe`  
		Last Modified: Fri, 17 Apr 2026 00:25:00 GMT  
		Size: 9.5 KB (9477 bytes)  
		MIME: application/vnd.in-toto+json
