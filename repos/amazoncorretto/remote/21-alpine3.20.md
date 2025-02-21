## `amazoncorretto:21-alpine3.20`

```console
$ docker pull amazoncorretto@sha256:d35e44aa90121164411d3f647e116d6c4c42461ba67dabc7c5ca6e460d380c12
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.20` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8577f8842811ad4bcedba215a3043bfa9bb97185e3753f4d116a4f9353f9f55a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.6 MB (162581841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6af4c09997ed318e377a77fac843a65bfc94a3b15705dc7cc963802dbb1ed721`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02989a25ce9487ba77b55af5ba3355e69b00dc52332d1da9ba8b1a028079d4d0`  
		Last Modified: Fri, 14 Feb 2025 19:12:54 GMT  
		Size: 159.0 MB (158954944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9a97fdcf76221200e7d14536533b9b022057f941444c9039caf18ad27b9d581e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **386.0 KB (385974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:359ec2b395d8ea6c2746de11806993df70d7394cc4249a07caec4c59e456f10a`

```dockerfile
```

-	Layers:
	-	`sha256:db5579b4ac2357ba0c2ce7169bbfd38cef219f7c9270a82f87b2ec3ffe162ace`  
		Last Modified: Fri, 14 Feb 2025 19:12:52 GMT  
		Size: 376.6 KB (376560 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:994009ce1914757be6ec8d984b4affa0fb0c05070c727873fedd766ea502b125`  
		Last Modified: Fri, 14 Feb 2025 19:12:52 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d41f69a7c4a92a3f7c2cb271987ab7a6f667a3a06dbe6bed0c9a22c44ef33246
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (161026199 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9f34d49d6b4d9625f04d9434a3355af4aab774e9396eb22135698bbed9b9df`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6252dc144cff56195a179795de38af252d3dda7a4d15db622ffc4e9ea0af6353`  
		Last Modified: Fri, 14 Feb 2025 22:39:18 GMT  
		Size: 156.9 MB (156935034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.20` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e89775cf5a65625cd16844dcbe695208446b852280476cbfc716510d0f653f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.5 KB (385497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ff757a7a3d3780554da53704393922d679485fb5c3e811a2f5f4ab2d4883ba`

```dockerfile
```

-	Layers:
	-	`sha256:bd4e833dd0950117466871c086b63e48e69595861735df2380299c3788492502`  
		Last Modified: Fri, 14 Feb 2025 22:39:14 GMT  
		Size: 376.0 KB (375979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddfdb9b782de9f0623bdc62184fe86f43dc1c0046273fcd407a515f0ac4a6482`  
		Last Modified: Fri, 14 Feb 2025 22:39:14 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
