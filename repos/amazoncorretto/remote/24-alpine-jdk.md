## `amazoncorretto:24-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:b302cc727153d75b4ad9587a496c6f4f3e5081da53f2a8c688ab61f75d7a73f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:c90b2dda8567d75f72a312602ecff0d1300126bd367b0e94e211ac85ae67e264
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180246208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed1fe7b935a226f5b360cdd7a05d27059a5638501760f65d05255f8ba2d1c454`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a48b65aa6e4c59dc2a9ecf9cd2b292e6627aa6a50fa6e96dac665e0d6f6e59c4`  
		Last Modified: Tue, 15 Apr 2025 23:56:10 GMT  
		Size: 176.6 MB (176603961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:25693c46c61b3642566b361a30feed8321df100e133c8120e828ff975557859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.4 KB (403404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21ea413da27997829d82f49e845936f690dd48af21c252428a2230ba1d3e60f0`

```dockerfile
```

-	Layers:
	-	`sha256:2210998828aed29508af559ae1020472933d14de643e3d79044c4e42d0eaa763`  
		Last Modified: Tue, 15 Apr 2025 23:56:06 GMT  
		Size: 392.7 KB (392684 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a1e14802150f50d435b475b75c0bf72d216a9ae510b1f09020de84763599f033`  
		Last Modified: Tue, 15 Apr 2025 23:56:05 GMT  
		Size: 10.7 KB (10720 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:8a478cab8777e19125cfb24f82bb548945303a5ba8093437897bef4f0df9b7e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **178.3 MB (178289785 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef8ad855e2ed1b11bfe356c1484bf0b7e38613badd742ffb57d2ead55282f1f8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36.2
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 21 Mar 2025 22:11:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 12:05:33 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b200419fbb2411dd3c011ec68c33ef49e2454e21c14a549aae4de7fb9256391`  
		Last Modified: Mon, 24 Mar 2025 17:37:38 GMT  
		Size: 174.3 MB (174296756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3fc4a60e5eba6177bf952e03167f54bedfea853f5c2a1601e6d8fa1d4b0a6118
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **403.0 KB (403014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:196c4889330cfc496a5fa5f5bee72d872ed364706cad937edacb4c0c5f487cb5`

```dockerfile
```

-	Layers:
	-	`sha256:24ffa8b68f75bac5bc649059a42109e9f56b260ee80d4dd24dc81d9da4941077`  
		Last Modified: Mon, 24 Mar 2025 17:37:34 GMT  
		Size: 392.1 KB (392142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:279fd3d69167e6d84d79f3062c37c046860d6656b5d9057d97bf3c4dcaabd2c4`  
		Last Modified: Mon, 24 Mar 2025 17:37:33 GMT  
		Size: 10.9 KB (10872 bytes)  
		MIME: application/vnd.in-toto+json
