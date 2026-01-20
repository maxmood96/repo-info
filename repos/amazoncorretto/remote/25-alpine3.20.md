## `amazoncorretto:25-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:04561d9321578b97007752e70379be28f7f58edce8f8a2cf6f2d161b07b9ff85
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:25-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1a8bbf81a298914b52c165271ffca01ae81899634b839569dc7be132adf72353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.3 MB (184339288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be9f15f17cba097373a6fb9f81e29101379af23f6ab8849618c99b31ceb157ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:03 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:03 GMT
CMD ["/bin/sh"]
# Wed, 05 Nov 2025 01:07:16 GMT
ARG version=25.0.1.9.1
# Wed, 05 Nov 2025 01:07:16 GMT
# ARGS: version=25.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-25=$version-r0 &&     rm -rf /usr/lib/jvm/java-25-amazon-corretto/lib/src.zip # buildkit
# Wed, 05 Nov 2025 01:07:16 GMT
ENV LANG=C.UTF-8
# Wed, 05 Nov 2025 01:07:16 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 05 Nov 2025 01:07:16 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:02:45 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a36c38f134e5625682b70fe904bf04aa14fb0074989d4b1de278ada124db33`  
		Last Modified: Mon, 05 Jan 2026 07:23:04 GMT  
		Size: 180.7 MB (180712232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:367bede86a628ab4ca2c89aa6d0248c6c4673e3bfaec494f350fa7ed5d825930
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **599.0 KB (599023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:488bb660d766f2f933ab2cc2711ecffe80e6c0d102f5c7e64cb1a23465ac9c31`

```dockerfile
```

-	Layers:
	-	`sha256:fdf97aec17dbde337452084f7450e1626b99e91350a33b3461e69dc6933a15d2`  
		Last Modified: Mon, 12 Jan 2026 15:30:01 GMT  
		Size: 589.7 KB (589653 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80c42549942fe2a3c72cbf9aec50a0bc3a696a1a92867bab499f218c27ba39f7`  
		Last Modified: Wed, 05 Nov 2025 01:07:33 GMT  
		Size: 9.4 KB (9370 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:25-alpine3.20` - linux; arm64 variant v8

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
		Last Modified: Wed, 08 Oct 2025 12:02:47 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d6104cd0079df7a256c2b1cfc3829b6bb49821af98f23bf4a42463269967a25`  
		Last Modified: Tue, 06 Jan 2026 18:55:06 GMT  
		Size: 178.4 MB (178375918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:25-alpine3.20` - unknown; unknown

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
		Last Modified: Mon, 12 Jan 2026 15:30:02 GMT  
		Size: 589.1 KB (589069 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48e5dfac80c1eade18f419287079c14b3b731329493cc028a340078afe8b86e9`  
		Last Modified: Tue, 04 Nov 2025 23:16:40 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json
