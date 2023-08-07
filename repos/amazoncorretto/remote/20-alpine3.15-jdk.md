## `amazoncorretto:20-alpine3.15-jdk`

```console
$ docker pull amazoncorretto@sha256:21503c16656b65f5f46d61016a1363fb74691a3ffd1ebfc216c43017d24bbd48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:20-alpine3.15-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0c715ae0d924f24c8232c531f1a4e6650e074ca73492642cca9545bf67f2c70f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **157.4 MB (157400835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:999c03a2cd5708630c63b5224f3bd30e90edbdc4468d0cbb363ab50fad8abcc5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:37 GMT
ADD file:4faae297b6caba92e1791a5ff667be0fcb4de6a4de2df155395957ef9d8ad5e5 in / 
# Mon, 07 Aug 2023 19:20:37 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 19:47:43 GMT
ARG version=20.0.2.9.1
# Mon, 07 Aug 2023 19:47:49 GMT
# ARGS: version=20.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-20=$version-r0 &&     rm -rf /usr/lib/jvm/java-20-amazon-corretto/lib/src.zip
# Mon, 07 Aug 2023 19:47:49 GMT
ENV LANG=C.UTF-8
# Mon, 07 Aug 2023 19:47:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Mon, 07 Aug 2023 19:47:50 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3695f6c099b80e503148dbb435d044c35147f81d34b9d6fbb27b3dcf1fd7ecaf`  
		Last Modified: Mon, 07 Aug 2023 19:21:27 GMT  
		Size: 2.8 MB (2826006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34243a12733d6eab003ff6342c910fc3f2465c8dcbac4147a7f8a8a4a8163ca0`  
		Last Modified: Mon, 07 Aug 2023 19:56:56 GMT  
		Size: 154.6 MB (154574829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:20-alpine3.15-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b0e3ef2e22674c7ddbb4fb5e1b2476f187e80e323f3c0b44410704219a9b108b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **155.4 MB (155382151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d7e3da6a38bf9c722f163923ae33a166be26cdfae3c263810a07ce07ab73c5f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:10 GMT
ADD file:2b463f242cb7bf946452bb4781838348ecbe80da144fbab09f51d7e050dc68f3 in / 
# Wed, 14 Jun 2023 20:49:11 GMT
CMD ["/bin/sh"]
# Wed, 19 Jul 2023 00:48:07 GMT
ARG version=20.0.2.9.1
# Wed, 19 Jul 2023 00:48:15 GMT
# ARGS: version=20.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-20=$version-r0 &&     rm -rf /usr/lib/jvm/java-20-amazon-corretto/lib/src.zip
# Wed, 19 Jul 2023 00:48:17 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jul 2023 00:48:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jul 2023 00:48:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:a147224bf413aeffbbfcdcb5104d35c647256a5c32083f4d8134f09a4e74ddeb`  
		Last Modified: Wed, 14 Jun 2023 20:49:52 GMT  
		Size: 2.7 MB (2720801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77c0d3e99ce95c8517962bde2d72e7eec25e760c0bcdf52932754c9a6f1708cd`  
		Last Modified: Wed, 19 Jul 2023 01:02:38 GMT  
		Size: 152.7 MB (152661350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
