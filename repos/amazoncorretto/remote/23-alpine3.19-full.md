## `amazoncorretto:23-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:4f2d5467eb07f3f7f4b6cf4802c175c0a6800480c5bd21e04ac57672674c2840
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:35af26594a4933e6e7026c83f546c1a973cfd1e1ba54644b3ed380a41e4326f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170109314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b7a6163bc22c5dff6394bcf498563cfcfdd0b4a9db5bd0ecad2a08e7d9c3bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=23.0.2.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=23.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb79ab6925871b297230cdec2780f2c43ca06b50cf10ebdd0c56102a93cb3426`  
		Last Modified: Fri, 14 Feb 2025 19:13:01 GMT  
		Size: 166.7 MB (166688446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b78e392229a160f93d8d6c004e740842bbcd741abed4428a5ec825799ba6b243
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.1 KB (392150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3fa4be952d4467c326db173b39a2e177f4ea8b8ba8c85215436acfca4599784`

```dockerfile
```

-	Layers:
	-	`sha256:2cf46a088b2653d79422e75850515da1adc70f01768aa9b3c4a7f5803d0f80ed`  
		Last Modified: Fri, 14 Feb 2025 22:49:17 GMT  
		Size: 382.7 KB (382737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f047de4b8d49c566f5bb3b6fe43f183c9e2d8de5d3c95709f01c9e34b5b0558`  
		Last Modified: Fri, 14 Feb 2025 22:49:17 GMT  
		Size: 9.4 KB (9413 bytes)  
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
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
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
		Last Modified: Fri, 14 Feb 2025 22:49:19 GMT  
		Size: 381.5 KB (381516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a44835e1545b2018b4c3fa57795893c4bb81d2d14cc5393f585af0ebf45d9c5d`  
		Last Modified: Fri, 14 Feb 2025 22:49:19 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
