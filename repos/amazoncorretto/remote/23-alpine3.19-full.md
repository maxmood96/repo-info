## `amazoncorretto:23-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:cc238de37ca4fa886e026250a315bbedd40c99676c81c4e1f8925a8b842c5636
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ba19c2950392409a43a4322f18a019bd987cad9500a7539e83800557ec3c77ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170108675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a0776732eea87cd9a1b363c0d7ad17dbf5cb65f52aa0f00a0fa8d89d78551e3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:760b60ef2f7bbf2131b9b5d67c65a3ccd44d2bcf9e04f11a54049de02144c3be`  
		Last Modified: Thu, 23 Jan 2025 18:27:46 GMT  
		Size: 166.7 MB (166688433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b5c58b3ae5a04251f73f9fd1fe0e7c28c4c7479cbaa3f68723ecd24ee1c58879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.2 KB (392151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82a7241a563194b4ef7bb95e6d0d66103e192c311e304b3a112751793d1905d8`

```dockerfile
```

-	Layers:
	-	`sha256:2e2a51c8917a62a20625820c356a6bfd3ed921236e4ad0fa5e4f0f9109422ade`  
		Last Modified: Thu, 23 Jan 2025 18:27:44 GMT  
		Size: 382.7 KB (382737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf86c4fe3d55d8ea3d06166e6a6487f0a0ca4e6207c50a942d8f6304b015de9d`  
		Last Modified: Thu, 23 Jan 2025 18:27:44 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1b2b088dc895e9ddc8387350c053f32865c1d25899b911f4b9426965bab3c7e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.8 MB (167769396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29cf4d4a3c24a7ee8831e4002368b0eb6e8da7c81abf905a13704524114d07bf`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=23.0.2.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f973a97d686f1d71aa5e483731c6b9412fc8bd8e72a53525de73a31c5e67d48c`  
		Last Modified: Thu, 23 Jan 2025 18:57:36 GMT  
		Size: 164.4 MB (164408864 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:abfb308a53bef11e30f27c7fa3f70e9d7c31f59ad3c997ca9e83cc6cc41bbaf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.0 KB (391034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78d068e51d81cd073a3076ec408e7d892da1d43690c28f281471219132cba207`

```dockerfile
```

-	Layers:
	-	`sha256:0929f98d15568d271169d3893c331d88d018f7d118b2e0a7cac3e92792381070`  
		Last Modified: Thu, 23 Jan 2025 18:57:32 GMT  
		Size: 381.5 KB (381516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a44835e1545b2018b4c3fa57795893c4bb81d2d14cc5393f585af0ebf45d9c5d`  
		Last Modified: Thu, 23 Jan 2025 18:57:32 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
