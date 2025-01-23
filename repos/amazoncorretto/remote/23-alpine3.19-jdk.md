## `amazoncorretto:23-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:5dfaf95962a8c306253b309004177bc1597c266ffca0b71e1e2f1aa7d2bdac03
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ab16acdce947787f18e423610e514c81b137077607d99910168c319111a800e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170078733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ebbd5192ab257eefd02d37ccaa22b6834be323924aa9e011426c8c7042e615f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26c46ea9748b6cc8bf6717b02f5054037b66f3c4f9f51370447839bccf239726`  
		Last Modified: Wed, 08 Jan 2025 18:14:46 GMT  
		Size: 166.7 MB (166658491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b6f70131794f94ccda90570885280d6b13fbe98e187044aeff117982bbc2378d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.2 KB (392151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cf1ecfa045ced229dd0eb1201698d04ea11fee761f699e92ad05735e495c3b8`

```dockerfile
```

-	Layers:
	-	`sha256:8392d218f932172727f0d2a0def46c2839ffbea7b072e1e47668bc1abe2747d0`  
		Last Modified: Wed, 08 Jan 2025 18:14:44 GMT  
		Size: 382.7 KB (382737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29feb383648a17573c185577203263069bd7b7ea1e7f93b10b60156e46a189a6`  
		Last Modified: Wed, 08 Jan 2025 18:14:44 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.19-jdk` - linux; arm64 variant v8

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

### `amazoncorretto:23-alpine3.19-jdk` - unknown; unknown

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
