## `amazoncorretto:17-alpine3.20-full`

```console
$ docker pull amazoncorretto@sha256:38b44a49bfd11b925015b281d3d35c845daaeca5f0e3827f8e1df9bedf7b256a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:77980ab89485cd9103fd2cf526e35ea39efdaaa412037c5118d474e6699661b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.3 MB (149304568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c5f66dac65810a9155e96beff12b28cdaf0a8ec5eee8551a5aa6b8d71e8e227`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 14:35:06 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0e9cf49a439c9ddc32e569232c6b6e1656b3e527ca85f0bd467aa815af8d46`  
		Last Modified: Fri, 14 Feb 2025 22:57:18 GMT  
		Size: 145.7 MB (145677671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eca857d499978269edea0c6e614601af6aa90cf85027917d03d236a9942db7b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.1 KB (386079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10de6a4f6fb304757c52921d63e04f2babc1ae954fc2b19598e150c6685bedfc`

```dockerfile
```

-	Layers:
	-	`sha256:1db56d7ea03f4239d63a2f81830ebec9768ab40b553319f2935b12f1cf6d28b5`  
		Last Modified: Fri, 14 Feb 2025 22:48:14 GMT  
		Size: 376.7 KB (376663 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59556c61100abfce8272d7eee91ee5aef39b555de4f4dab071697fb64cb28fb`  
		Last Modified: Fri, 14 Feb 2025 22:48:14 GMT  
		Size: 9.4 KB (9416 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9eb984923d905af57d6b550a0a7820d33b022d3a8d4f8ae39c9589bbd7be96ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **148.1 MB (148111577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216152d4e787011fc8c6c29aa33a5b1bd1cd7e8c574cc7864f3133fc8f3296d7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=17.0.14.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=17.0.14.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 14:35:45 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8e4ebd0ca3766fb80eec24cda9421e493b75b1b14eb49c95370c890792f03`  
		Last Modified: Sat, 15 Feb 2025 18:33:56 GMT  
		Size: 144.0 MB (144020412 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:80665e0dfb644821339e2049fb6d36fd5348742f2743ba67547e46a1c7b474b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.6 KB (385602 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdae3e5eba4049124fa5108168e91d32b3de84f7b8869387f1a02ef9a07bf39`

```dockerfile
```

-	Layers:
	-	`sha256:f2716c1fc5b6faa1f5fc267496d74ae17760748b16aa6379f24b24eebda93b4b`  
		Last Modified: Sat, 15 Feb 2025 01:48:14 GMT  
		Size: 376.1 KB (376082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e8cc3539b9710d5aa21bc656cc4d8760b173cdb0c4c444d7eb8bbbfa76cdb4b`  
		Last Modified: Sat, 15 Feb 2025 01:48:14 GMT  
		Size: 9.5 KB (9520 bytes)  
		MIME: application/vnd.in-toto+json
