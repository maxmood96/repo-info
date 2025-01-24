## `amazoncorretto:17-alpine-full`

```console
$ docker pull amazoncorretto@sha256:73181c9bfb28bab7a775f6974c542f690f1b71d333ea5f75efa79e45a6726bcf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cf95ba801a82e620650d572b90bd4983090ece351f727421b99c9029ac0ec807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149303956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77e7e3f5b13913b143910c946d29b0f704f77ab506ffab8baf10616698fdb8d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Wed, 08 Jan 2025 15:55:45 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96e52eec5ee29c3c824bd2383712108d8ee1270ac47a8648b81367bd14411b1b`  
		Last Modified: Thu, 23 Jan 2025 18:27:13 GMT  
		Size: 145.7 MB (145677696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0d9dcc004c592efa51e7275f2291c0416374d7aadf03346108d21b8e13e250e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.7 KB (388696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9826ad0f2256fb577bb55c6e04e63f1d92fa7bc25a7be21e4de5f9057eb5a4b`

```dockerfile
```

-	Layers:
	-	`sha256:a839680ec249cc2a70721849371fba284aba02ca7447f0adced35d643a740e8a`  
		Last Modified: Thu, 23 Jan 2025 18:27:11 GMT  
		Size: 378.0 KB (377971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab0a9af155c3fa5dbbc8e945f9fa36c1ba1733459cac8914089e86aa2dc02e70`  
		Last Modified: Thu, 23 Jan 2025 18:27:11 GMT  
		Size: 10.7 KB (10725 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:6554290c6cc021a19548e21470752a47b066197587263c312bd2e093536d46fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148111671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994b525b664575c693b10eb4fba81a8a314c626d71bbd04ff8ef2401ed4c552b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:08:14 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:08:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=17.0.14.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Wed, 08 Jan 2025 17:24:05 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31bbfd5bba38b947d2ea3a0b77869ef0e6f42408ae61bf467f85d73d093edf4e`  
		Last Modified: Thu, 23 Jan 2025 18:48:50 GMT  
		Size: 144.0 MB (144020902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5cd2c607bcf8b84685540471ec3a45434b34741cc3125eb2abed864161e44fde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.3 KB (388314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7829d69e066c24bfe7d209edf61af81c49048e10c2ef5c3fde6e2a3f98c3c90`

```dockerfile
```

-	Layers:
	-	`sha256:62e32a01b3c9756c040e81e2c323a6567e10ad2d35a761bbc02d8a8051e0eadd`  
		Last Modified: Thu, 23 Jan 2025 18:48:47 GMT  
		Size: 377.4 KB (377438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99bbd23312ee4e1f9f080bbf3a866445aac021fa52f1c00d36b534324ed6d4b8`  
		Last Modified: Thu, 23 Jan 2025 18:48:47 GMT  
		Size: 10.9 KB (10876 bytes)  
		MIME: application/vnd.in-toto+json
