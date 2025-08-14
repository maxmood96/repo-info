## `amazoncorretto:24-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:ca2e9303acfb887e1b87733aa55bcb3af412389be4a2c207b37bd47015ffea13
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6bb02e15482f7cf9f62c8bdf99999012d3ed85d83866c0269b95598f9feb5fc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.2 MB (180186006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf46118702578ce5365e4db79e604827d069fb7d4be90149d1e9577be658198`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=24.0.2.12.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:1747dece94917ce1b0256ecd60138ce4deaea1bd35dcb6b2e8afe697dd2f5b71`  
		Last Modified: Tue, 15 Jul 2025 18:59:51 GMT  
		Size: 3.4 MB (3415528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31fca68e03c5745d2f9296346dbbc74c0600a36d08bd0732697b170bf5c4d2c2`  
		Last Modified: Thu, 17 Jul 2025 00:16:26 GMT  
		Size: 176.8 MB (176770478 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:46541850e5a2e49395bc33d7f3e4ff7f8a1cb1209ba8b1b445f442ee8be7cd1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.9 KB (400890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12288cd06985e68e718e7a5fbf18ca4322ff1ee41f7e1af93eb0f136fdfaa9c4`

```dockerfile
```

-	Layers:
	-	`sha256:97e0e4d9e45d392ffc9c99e554d747e265c49a96cc81eaed88809048d3be9900`  
		Last Modified: Wed, 16 Jul 2025 21:50:36 GMT  
		Size: 391.5 KB (391477 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a7f6794ffd36eba67fa2eb7c6985baa20538499e7381af066440f2340337aed`  
		Last Modified: Wed, 16 Jul 2025 21:50:36 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fb25e7a6fc49dc29119baf4f4a01fca1df7dc512873f76a0f43d3c423c0987ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.9 MB (177870188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d27cb2ceb76388699e2d62fd223738bc9372d39295f6488d34eb32aaf67e4eae`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 15 Jul 2025 11:32:09 GMT
ADD alpine-minirootfs-3.19.8-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:32:09 GMT
CMD ["/bin/sh"]
# Wed, 16 Jul 2025 19:33:24 GMT
ARG version=24.0.2.12.1
# Wed, 16 Jul 2025 19:33:24 GMT
# ARGS: version=24.0.2.12.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Jul 2025 19:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 16 Jul 2025 19:33:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Jul 2025 19:33:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:07e9a47f0c334cceba1b05e86ef0150c84564a9b9e9d4ae9dc9a5ebc85ef2b7c`  
		Last Modified: Tue, 15 Jul 2025 19:00:19 GMT  
		Size: 3.4 MB (3353103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c8e745b6706266b3b28a32019b5a275f8956d24ffff7014f6cca36848754e1c`  
		Last Modified: Thu, 17 Jul 2025 09:09:03 GMT  
		Size: 174.5 MB (174517085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:775c4f945c3c628ab0d3d84eb81b623656b2281b6066356675693476a31dfd79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **400.4 KB (400411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:007f39b23fb05388cf428377e8f1cf0f457a3513a81c4c27e0918805ea77bd7c`

```dockerfile
```

-	Layers:
	-	`sha256:87f2ff06c97100ebf0b9fa4a6cccc0b8892689a6e5180aac9484423dc9a7f1a8`  
		Last Modified: Thu, 17 Jul 2025 03:50:28 GMT  
		Size: 390.9 KB (390893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44f9d2ee4d95ecaca8ce8d1836bc80c2e1d4ee590eb3e6e5b230377ee9a0eb2d`  
		Last Modified: Thu, 17 Jul 2025 03:50:29 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
