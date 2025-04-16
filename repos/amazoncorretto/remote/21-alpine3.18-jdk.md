## `amazoncorretto:21-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:48c9e932700144281f358c2b8064028ee287b5d85173c589d6c0ba80903aadae
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fd4aa81bb04fd172019b5170e41e591c6d85a985ab7efa5b658dcbc37b882666
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.5 MB (162451230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc4c010d215b7ffb024514f47135f09ae43970c288de4d142afe147f202c65a3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:03:06 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=21.0.7.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=21.0.7.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 12:05:05 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00dafba695643a64ad97c0b5be7979ea4effbf199f23b1a9eb9f8862c8449bd`  
		Last Modified: Tue, 15 Apr 2025 23:55:43 GMT  
		Size: 159.0 MB (159032821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:234dc5e93d51e0f69949580d42dbd6381b7b17a9c35ea184547dfba7e7257d08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:500465a8378c2c27a932b93d478c3a7e0a75637e8c7f851439893be8da68e0b4`

```dockerfile
```

-	Layers:
	-	`sha256:fc0608cf9831ad5b37e2cf2f23073c56a7d245a9e82c387ec40713abd322d1d1`  
		Last Modified: Tue, 15 Apr 2025 23:55:41 GMT  
		Size: 380.1 KB (380131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77b16a7cf2a3db727a42a8a550bd7301fe6fa34034e63e631138aff1eb001c28`  
		Last Modified: Tue, 15 Apr 2025 23:55:41 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2188d777bc38a4594078895a9f993a70d0ed4b18fab7b9527bb3d4206309f8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160277912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ade29438bd9b1f3265bb6ebdefa915857d545de6ec03941d574f0c7b29ef0b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
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
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 12:05:04 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb26e9488702b1357ffac101bd6980632413196a086cf4d151cfeb2c05b88b95`  
		Last Modified: Fri, 14 Feb 2025 22:38:12 GMT  
		Size: 156.9 MB (156935255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6850ee62a1c0fb62922178163d3fac2905b3c0844fc942a39609212f305a26c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.1 KB (389068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db32e9bd04c6a564ec2736fce78fde8f130d46dc4fccaa19608dfdaf6089e104`

```dockerfile
```

-	Layers:
	-	`sha256:eadc390d97263f6bccd6bd1f1c7fd0642aada2bfe7ab02512254d426ed5beec6`  
		Last Modified: Fri, 14 Feb 2025 22:38:09 GMT  
		Size: 379.6 KB (379550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d55c000d8d27de54957e5ea406f6d5f564c9407c3cfa1d2d5b004ce29201f89`  
		Last Modified: Fri, 14 Feb 2025 22:38:08 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
