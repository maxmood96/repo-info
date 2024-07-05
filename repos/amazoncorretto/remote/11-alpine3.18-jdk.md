## `amazoncorretto:11-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:2c96544a93e9aa9b86a06e68da66186afc6179b1d6bd58283bdac6fe1fb1ec5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:62b548d0cf6606f174dc685c036fb1194ec40a2c48a89ca16b637410156e2c50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.3 MB (145257528 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c1f740e76d0b6b604cab4a61e907f933b26940ed8bc8f0e66ca5bddd0977704`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:aa183dc07d0f6a47c02f7f1388fa0ce4639ad328111172149be7c7c65d634ded in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:73baa7ef167e70f1c0233fe09e741780d780ea16e78b3c1b6f4216e2afbbd03e`  
		Last Modified: Thu, 20 Jun 2024 20:17:53 GMT  
		Size: 3.4 MB (3413894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad950e8aba6cd47c98fe6abe6b6fdfc9813abcfcd6855f472213c1c0e93ecd28`  
		Last Modified: Fri, 05 Jul 2024 19:56:13 GMT  
		Size: 141.8 MB (141843634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5bab240015834e748d4121629c9d9f6d7587c306fd14e37cfec34a9065b39449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.7 KB (392713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32b7141998bcd9d3df913300352e8eebfdb4b7bf193b1bb6b9d9130cb45408a5`

```dockerfile
```

-	Layers:
	-	`sha256:badedf5fff266728d0475976a579eccad9793dc17ab49e9b6fc534d9174842d8`  
		Last Modified: Fri, 05 Jul 2024 19:56:11 GMT  
		Size: 383.5 KB (383541 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92bc993eb3a48b0024b0c3bcd82181bad6eb140bd361ad0f05705f0e15aaf3fb`  
		Last Modified: Fri, 05 Jul 2024 19:56:11 GMT  
		Size: 9.2 KB (9172 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5efc2d77e7b7e89dd289fe5bf60859e772ceea4ce19d4bf7a1a078fe9f87f1d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.3 MB (143270491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e9d43669112edb10e1a54997ef4ae28924c2e60d6de19de5278eccca55700f1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:4f760ede9d48d6073317cae6d632deaab101f337e09c56a7f9b8847ed99de3e8 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=11.0.23.9.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=11.0.23.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5c905c7ebe2fecec0b1115f145c0ea74b3233aa25d8239903194f6b4424044ce`  
		Last Modified: Thu, 20 Jun 2024 17:41:31 GMT  
		Size: 3.3 MB (3337949 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4711bc6686972b7cbbe14de3ec89692927362a862057f228f90b6411e483cfa3`  
		Last Modified: Fri, 05 Jul 2024 20:09:54 GMT  
		Size: 139.9 MB (139932542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:862326d723d7cd7d8ad69fc00d824779131c28acc22d707dfac213788ea65030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 KB (393069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d13645ddd5151033e1f32c8adb786f78f227abdaf4f61d07659519e12cd882fd`

```dockerfile
```

-	Layers:
	-	`sha256:37fc9d89e8a6f8299d2275d2d4938274c88a33e0a78a428f3076d5d368f5a2bf`  
		Last Modified: Fri, 05 Jul 2024 20:09:50 GMT  
		Size: 383.6 KB (383597 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e0ed0e3969fa19dffefbdaf988073c7436883292b125f4ee8d9af426098a1a7`  
		Last Modified: Fri, 05 Jul 2024 20:09:50 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json
