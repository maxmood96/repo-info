## `amazoncorretto:8-alpine3.21-jdk`

```console
$ docker pull amazoncorretto@sha256:3f90cc1ee4454c08f61c76d2c39ac7ea86045111bcab8371731638677a3684c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:842f3eb104513a2152076c8f2051f0c868052e538fac3fc2357c5e4d46584660
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.4 MB (104422874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5118d4c250a45e307adb35ed005408116d9291d5aaa18662f232ec5fd7d8aa77`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:15 GMT
ADD alpine-minirootfs-3.21.7-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:15 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:07 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:22:07 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:07 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:22:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:897d797d2723cf0e318402f4d6f37d51b011517e5cf09246b22155f0fa90dc81`  
		Last Modified: Thu, 16 Apr 2026 05:32:55 GMT  
		Size: 3.6 MB (3646875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2d5a68985d86fb46cd3eb177f0f213ca668d0d60316f0d0844c46a80198ce8`  
		Last Modified: Fri, 17 Apr 2026 00:22:21 GMT  
		Size: 100.8 MB (100775999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e54d764285a42bbfc16357e4a78ccf81ca2cefd8b980f631358a0d65756ef15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.3 KB (260287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22128b599dddae7fffc951755150fd67682208bb5717935ff0ec11f32e4eca1c`

```dockerfile
```

-	Layers:
	-	`sha256:c830812a00abfedda8fa38186540b4f9bad63c0447be1c1359ab6e06bed0bac9`  
		Last Modified: Fri, 17 Apr 2026 00:22:18 GMT  
		Size: 250.9 KB (250933 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d31f389a8fbea9465578da15543598974fbb04674677d0fddaad1968401ba50b`  
		Last Modified: Fri, 17 Apr 2026 00:22:18 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.21-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:595ca1ea70da45890f05cb83299d728f79c1e3acbf34da839518f176695ead3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104556615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55ec1c24091d73052903c94934b8955316c7160f2dcc80ca968ae54e7319e7c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:13 GMT
ADD alpine-minirootfs-3.21.7-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:13 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:07 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:24:07 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:24:07 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:24:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:24:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2dd7199cff98a7400e801cbfad6de906972a4e3dd0a749d4c1b80f5a1e3e4108`  
		Last Modified: Thu, 16 Apr 2026 05:32:50 GMT  
		Size: 4.0 MB (3994465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1898dfe04ced66c52d23440892c5686be9f1c94573725c15d80b4b66a0857acc`  
		Last Modified: Fri, 17 Apr 2026 00:24:23 GMT  
		Size: 100.6 MB (100562150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:30ee224dfeec50e7579ec96f83b02b8e124da820c42c7491c24bb21de0810616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.5 KB (260524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5d90d264c407f77ccf10c4b3c9a1e096ed3957a2f8ae46050698de1ab614e4c`

```dockerfile
```

-	Layers:
	-	`sha256:7f3bc90382ae5de38bded0245896a55fed9d324e6f8d8b956e61781cd41fb674`  
		Last Modified: Fri, 17 Apr 2026 00:24:20 GMT  
		Size: 251.1 KB (251065 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9d3aea0a7a66e60e549be5bca86a21c1b4d52075e3215138273531f03ff4075a`  
		Last Modified: Fri, 17 Apr 2026 00:24:19 GMT  
		Size: 9.5 KB (9459 bytes)  
		MIME: application/vnd.in-toto+json
