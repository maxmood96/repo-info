## `amazoncorretto:8-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:20e72c33fb612721c394585a9c56fa52208d22d4a8bd5a829a5f6dce4eada5ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9e80ea7f0483057b00a7915f995498d92eb3c81d57dd4e4586c04b7eb3020e37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.7 MB (103666943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9bf04e0b1a7399af74398588769dea82ac4497a17b5aca9650fa4f7d46bda5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:03:06 GMT
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
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 14:36:09 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d7605c635fe12431a15df62ad6c6c7a02b4acbcf4bc497e83effdd385a399a5`  
		Last Modified: Thu, 08 May 2025 20:39:29 GMT  
		Size: 100.2 MB (100248534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3176b9389ebbe49d54b30efc6367716e020d3b46c97cf47087a9d787b5e60743
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a456f8ba20fab55dbd4968c3fe4abb86cfb4bca0a189d2a1472e9fa12760f0d`

```dockerfile
```

-	Layers:
	-	`sha256:7d3743de0f5c88c0c0e781fb336561a1031b94dbafdfce92564b853e9aa4e746`  
		Last Modified: Tue, 15 Apr 2025 23:55:16 GMT  
		Size: 245.0 KB (244973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3526833905de5b0b0dce309d04c270a98bab8e26bb39e862e4414145269c9d2a`  
		Last Modified: Tue, 15 Apr 2025 23:55:16 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a09a2aac80369e7f8c9ebcd6f3dd5ef3c6030d262ebb855dc7b6cd5412005cc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.4 MB (103359180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0f34fc82cb3a82c99fcb3e26b2d04295f4497ad5129397d80c32d3a7d31074`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:03:06 GMT
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
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 14:36:47 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:235679c8a8d8a6e1a66c4bdd7b23f44afc17bce89a0a1df50d56616625d79e7e`  
		Last Modified: Fri, 09 May 2025 10:10:51 GMT  
		Size: 100.0 MB (100016523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4d014bca9eb526d2e29c9ea0acd4b7d8e5068b36d49fbbcbcd448b7737693674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254607 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4135760228694c529bc58c15e52fd8247cbccbcecc642e8e5527efa4ce67a2e7`

```dockerfile
```

-	Layers:
	-	`sha256:d3d59e39753f54915dbb2ab6aff1ec0a163880bcc701bff088f39a05a5f15b85`  
		Last Modified: Tue, 15 Apr 2025 23:57:55 GMT  
		Size: 245.1 KB (245105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80dc620de2b3c0f5bd6d64f2d19851e07b1aac64a9943e8d7eceff8b762748a0`  
		Last Modified: Tue, 15 Apr 2025 23:57:54 GMT  
		Size: 9.5 KB (9502 bytes)  
		MIME: application/vnd.in-toto+json
