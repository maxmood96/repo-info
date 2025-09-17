## `amazoncorretto:25-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:4ded785a7f3df83c30e6476c6625dc23c52f72b60d762611d230331e62258cd1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:f0c81631447e17cc8d82e5bed58a555e6c4d5406be98715968c5406c550ba588
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.1 MB (182144690 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed32e604215550a2a55075cec79d8c9cf44cadc7bb0be7d1623ed4301e8ebd80`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:01d036902a3ca86e8793073c8094cba44d83a38953a489ac0641f3de017fe2d2`  
		Last Modified: Tue, 15 Jul 2025 18:59:48 GMT  
		Size: 3.6 MB (3620477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b532632fd1a28a4ca179507f11c4f7914e41fa22d7c8bb12b4d0611e0d5ae34b`  
		Last Modified: Wed, 17 Sep 2025 18:59:08 GMT  
		Size: 178.5 MB (178524213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:285bb0715302597d54c2244713e3c27b86be58d7ca088cf38c7c915635600032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.5 KB (396487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d6c5782ce9674672f4e43710bea12cf6238d31b77b4b05d594ccab326db359e`

```dockerfile
```

-	Layers:
	-	`sha256:2a395f2637fd8e5967c1631b0702e2cb1d4d576ccc8ff024368267f89274a73d`  
		Last Modified: Wed, 17 Sep 2025 18:49:07 GMT  
		Size: 387.1 KB (387072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b33ea508f84caf46ae36b33ca3b0ad639023b5b5cb209db6cc9afb88bfa5fb8a`  
		Last Modified: Wed, 17 Sep 2025 18:49:08 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f3700bcdd0ec8a54147bbff8cdb6013335ed51fdd9564cc21f9fb80ace24e44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180160608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17e168a393481d3509ea94f31c73cfd2a12e7ce76b726aacf6df777e6cabf08`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:31:35 GMT
ADD alpine-minirootfs-3.20.7-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:31:35 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=25.0.0.36.2
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=25.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:13e713f825654e9e4f57146ec84918d478434f708d4d3d9d18d0e7ba2be56801`  
		Last Modified: Tue, 15 Jul 2025 19:00:10 GMT  
		Size: 4.1 MB (4088368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32aa498bf18f90c297094c56ac1e96e8dd85a28215b1b0c2bede51bf7952aff6`  
		Last Modified: Wed, 17 Sep 2025 18:59:06 GMT  
		Size: 176.1 MB (176072240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f68070a0904bbc374addce6666bb6499855d919ef623be056b21f5654a8f2366
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **396.0 KB (396006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78c17b50a88470f48392eeb590b03031458a4986508ba61c6d827753d915f5c4`

```dockerfile
```

-	Layers:
	-	`sha256:7e7c726246ca898eace51bc31b1d35238ba876c517bef7784c34c1956428e3ce`  
		Last Modified: Wed, 17 Sep 2025 18:49:12 GMT  
		Size: 386.5 KB (386488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f74dc2dd5cc4adacb3ebe65a50ea048eef3671726a655cb76f00a0099ddb756`  
		Last Modified: Wed, 17 Sep 2025 18:49:13 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
