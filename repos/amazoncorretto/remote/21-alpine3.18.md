## `amazoncorretto:21-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:e4dcad72b51013a5649fdf042ba01275853daf7343ee6946717740997916d56f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:29263a8c3b3f6b7c31bfeb1642d2266bd23f30a4e25bd3747fe148a5ba803a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162373704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f505819796c41c45baa73a53ec1550684525c72ef67c05181bab5afc8dbdb5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7793d961ab18f6c31d4f9e6b51af809c83b4158296608bfb983af58c71bb480f`  
		Last Modified: Fri, 14 Feb 2025 19:25:11 GMT  
		Size: 159.0 MB (158955295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5b713eb710dd13acab0dd3fd129ce42b042e1daa7dfafc38a99f59b5414b6384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32a0ffb49bb80837fa584030abc9be4509d3ac5e805f38143f62a43190ae985`

```dockerfile
```

-	Layers:
	-	`sha256:aca3a849c026a47728a9a1703f34f931828a544f816c12eddee211fa5e648df0`  
		Last Modified: Fri, 14 Feb 2025 19:25:07 GMT  
		Size: 380.1 KB (380131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ece7656e423114e4b681148c26a4fc02082003fa314718f15885ffce7fcced9`  
		Last Modified: Fri, 14 Feb 2025 19:25:06 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2188d777bc38a4594078895a9f993a70d0ed4b18fab7b9527bb3d4206309f8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160277912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ade29438bd9b1f3265bb6ebdefa915857d545de6ec03941d574f0c7b29ef0b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 12:05:04 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb26e9488702b1357ffac101bd6980632413196a086cf4d151cfeb2c05b88b95`  
		Last Modified: Fri, 14 Feb 2025 22:38:12 GMT  
		Size: 156.9 MB (156935255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6850ee62a1c0fb62922178163d3fac2905b3c0844fc942a39609212f305a26c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.1 KB (389068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db32e9bd04c6a564ec2736fce78fde8f130d46dc4fccaa19608dfdaf6089e104`

```dockerfile
```

-	Layers:
	-	`sha256:eadc390d97263f6bccd6bd1f1c7fd0642aada2bfe7ab02512254d426ed5beec6`  
		Last Modified: Fri, 14 Feb 2025 22:38:09 GMT  
		Size: 379.6 KB (379550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d55c000d8d27de54957e5ea406f6d5f564c9407c3cfa1d2d5b004ce29201f89`  
		Last Modified: Fri, 14 Feb 2025 22:38:08 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
