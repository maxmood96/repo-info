## `amazoncorretto:25-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:dc99751e86f098e2a1585ce2f67a928aacb86b0645ce10b03a4aebe021ce4325
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1b83fd6db358ae2f335e517609029065ab17c45dd0939bde1e5278ecd9d47f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184337221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb4b11e480f6e9f778fd17a7b52ea8695a1bf27339c838519533bdeddd230f8d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=25.0.1.8.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=25.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a168f027bb57f92b736bb567d5cff668055ea4caa3a75c69c013fae72cb3ae01`  
		Last Modified: Wed, 22 Oct 2025 02:07:33 GMT  
		Size: 180.7 MB (180710165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:91f2836a6f3ec180ef5e8c6d81b76885fa705acb695667a1b120a2e6ae835d97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.1 KB (599067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aaec2880610f593e26ac2af668f9fe9283e1c146c41239fd04ea0a893fef498f`

```dockerfile
```

-	Layers:
	-	`sha256:ec8580e15e65e8700b8da8a74d91dfac15a27a30ba852350f6e3a79d0b7d0973`  
		Last Modified: Wed, 22 Oct 2025 00:53:58 GMT  
		Size: 589.7 KB (589653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5e437585f290ab0fb8e3d2bd143d7d941d4900b4957ae90ee99a0cb73a59e4f`  
		Last Modified: Wed, 22 Oct 2025 00:53:59 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:966d058646f31acfd83b4eeea4ad7b8c2e1947b87945b771093580f3e3ea0478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.5 MB (182465295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e657ba76765c7798b9af202c6e05198006c2c015111f1b4912a7c9c2d96a3819`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Tue, 04 Nov 2025 23:16:22 GMT
ARG version=25.0.1.9.1
# Tue, 04 Nov 2025 23:16:22 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Tue, 04 Nov 2025 23:16:22 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 23:16:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 04 Nov 2025 23:16:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6104cd0079df7a256c2b1cfc3829b6bb49821af98f23bf4a42463269967a25`  
		Last Modified: Tue, 04 Nov 2025 23:16:44 GMT  
		Size: 178.4 MB (178375918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7e4145adf3b160e850781eb3fc72100a96b8ea734090a1bc95b6a8c9ae396ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.5 KB (598544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bf1ae500c7b54203784ff21184feab93e0a29a39b8a728546617c118030c939`

```dockerfile
```

-	Layers:
	-	`sha256:555f464bff75bf43cb7df5576803e19c2cffdf0d4bfc4f3d636a804d8f7e2410`  
		Last Modified: Wed, 05 Nov 2025 01:50:08 GMT  
		Size: 589.1 KB (589069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e5dfac80c1eade18f419287079c14b3b731329493cc028a340078afe8b86e9`  
		Last Modified: Wed, 05 Nov 2025 01:50:09 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
