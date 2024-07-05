## `amazoncorretto:22-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:f60bd936503826b3e75a2d343b7385124d4c353ce3ad0c321f2d0478badade32
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:4a5bb318396ae9ee18050a9f0981ccbe900d7264d0b3d851e8b4cef67a1016e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161501762 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5c6367e1d2eaf7a73511f394c50a3704316810e9de728c670d63adf7f6fbe3e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:fb066571462e703f86645131b43d211ff8531ffac77ea394456bfe569a6f17fe in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=22.0.1.8.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=22.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:b84a74cde5af5c5199bfc2ce2a8c8951a29a7716d17327e923f1a14c870a858b`  
		Last Modified: Thu, 20 Jun 2024 20:17:43 GMT  
		Size: 3.4 MB (3417332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e37b5af350217fc65d5d622c6ce66c9ec635f5d387c29f6551e8535d672849`  
		Last Modified: Fri, 05 Jul 2024 19:56:44 GMT  
		Size: 158.1 MB (158084430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b184a4e8f7d08e020343060a8d874be6fde5ab5487c6011098e6e61f46235568
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.7 KB (389663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd57fbec57303a0b0c311b1350c3dacf9b232d93650ed3f474ded4ff84c1a97`

```dockerfile
```

-	Layers:
	-	`sha256:e52a4f95fd7db9993a2ba2ae7e07e921e380459ca6f891cbb561157fbffad10f`  
		Last Modified: Fri, 05 Jul 2024 19:56:40 GMT  
		Size: 379.2 KB (379189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6bc59c5dc74c61da36850e6946852f65212848efbb1478df09fa965a39c1d1e9`  
		Last Modified: Fri, 05 Jul 2024 19:56:40 GMT  
		Size: 10.5 KB (10474 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:b2ccd30a69c50a0c92dc7a5fa9e181a1d5aae27ef35bd487a49eae66002a38d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.8 MB (158791841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:077b4cd8adb4961bf513c21ce97a6ec678bb6c7c21dc4b2727aa5e4b49edd7ee`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:f5632bd5469a9b26f7ff1739bb0b5dd166613259104f7bf76d587a8a428debcc in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=22.0.1.8.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=22.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d4f2d2bd5ed999e04bfbfb910f14154b488ad32abf053954bff805f47fc3ad1e`  
		Last Modified: Thu, 20 Jun 2024 17:41:12 GMT  
		Size: 3.4 MB (3357202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6567eb059569db6561f3e76ad5d56c1dd19e0d26d4234e74e29e7039959ab5e`  
		Last Modified: Fri, 05 Jul 2024 20:32:52 GMT  
		Size: 155.4 MB (155434639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7d1da60e7ffb5a43a398462603cf684ec994bc6de8a59ca21f7575e7b01f65f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.8 KB (388837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdff47854b6a0635415201b66aeedc5b12610f11f1bf69cac00fd5b4a5217d0`

```dockerfile
```

-	Layers:
	-	`sha256:78ff2c3f51be09437f5f0ebe8fbd377be36d61c7106d9af2983a08df23ff1503`  
		Last Modified: Fri, 05 Jul 2024 20:32:48 GMT  
		Size: 378.0 KB (378014 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc93dfee062c62136678c69fd9a9814cfc224ce561f177fdf2a61657e1c496ab`  
		Last Modified: Fri, 05 Jul 2024 20:32:48 GMT  
		Size: 10.8 KB (10823 bytes)  
		MIME: application/vnd.in-toto+json
