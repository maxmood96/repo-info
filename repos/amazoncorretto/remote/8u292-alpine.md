## `amazoncorretto:8u292-alpine`

```console
$ docker pull amazoncorretto@sha256:73939d6cb017bdb3885ea35ae18af6c6bf403ae0000b25e59c84b1e95ec9ffea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u292-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1a3472c57788ef9c33e2b830bea1f5227562e197aac294e3b27305c4a3429b9d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101815532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a49dc0e3993ba2b79800dfa61af11876aad3ac15bfb8d280b35e81049b7a6ef3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Tue, 20 Apr 2021 23:20:11 GMT
ARG version=8.292.10.1
# Tue, 20 Apr 2021 23:20:19 GMT
# ARGS: version=8.292.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Tue, 20 Apr 2021 23:20:19 GMT
ENV LANG=C.UTF-8
# Tue, 20 Apr 2021 23:20:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 20 Apr 2021 23:20:20 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ec31fbf474c99d6924bc337c81bd4bfd0bfadb5a7e318c5456a3e110d4e9b9`  
		Last Modified: Tue, 20 Apr 2021 23:22:28 GMT  
		Size: 99.0 MB (99014965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
