## `amazoncorretto:8-alpine3.21-full`

```console
$ docker pull amazoncorretto@sha256:296c2c4897ba90c1db5c980263b5008a17320de56fa995bb35017d9798163327
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.21-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:27766d58a0c7acd06713f0c5b7c16c215d1bf7ee835e7c89ee161069692d32f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.9 MB (103890933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bfe5f2825198a32ff42f1f3e365c887c65b38447f8e73491e0f15453ea55c54`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=8.452.09.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=8.452.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c4a12d4db20ff4ae3292effdd67698d13ada936fd200050caee895507b0f111`  
		Last Modified: Thu, 08 May 2025 17:25:08 GMT  
		Size: 100.2 MB (100248686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:be743b35f61a1357a3dff5d02841ac0fefef4df63a6202f6c276fe31ce2f63b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.1 KB (259122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05933b142b61ea6a6ae14262879eded34b759109b412db19c229d5405a65b634`

```dockerfile
```

-	Layers:
	-	`sha256:129b98fc4153fa961280e3f611b0809cf3f0843c39080c81e8579411ddb67070`  
		Last Modified: Tue, 15 Apr 2025 23:55:21 GMT  
		Size: 248.4 KB (248426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf68e04ae9a7c21d97a09afcaad6e02d7d0316b965858e841f8c9c23fef13477`  
		Last Modified: Tue, 15 Apr 2025 23:55:21 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.21-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:65af7b67f3c7dbd47b2ff9d809ce994d7aed04659c0ca612559badc43d00af03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.0 MB (104008850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec4a3c1d9d519a95e3f1c669cca05919cca39848068603dc14a8212b6d402fd6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=8.452.09.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=8.452.09.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4df05e124139c9c5577ae5800a072d376fb0f7147493ff51fafd79368b99c005`  
		Last Modified: Thu, 08 May 2025 17:25:11 GMT  
		Size: 100.0 MB (100015821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.21-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:0ffd71f7a64aaef24cf4a819f6d445b2c423af817d71d47b453bf2e6bd736159
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.5 KB (259454 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d73e410a88d7b68302ee197fa161cd769feddbf7585645806ceb1f751dca9b3`

```dockerfile
```

-	Layers:
	-	`sha256:5c5f3e4dc91abd5034fba4d9e3fe4b954def1c833d7f27f86d8fef10cfd2bc49`  
		Last Modified: Wed, 16 Apr 2025 00:00:11 GMT  
		Size: 248.6 KB (248606 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b507c87db692a0a7fef4c8575580586a239ae4c49c6f33176028dfe11f991069`  
		Last Modified: Wed, 16 Apr 2025 00:00:11 GMT  
		Size: 10.8 KB (10848 bytes)  
		MIME: application/vnd.in-toto+json
