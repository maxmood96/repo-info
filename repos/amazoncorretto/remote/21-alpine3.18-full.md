## `amazoncorretto:21-alpine3.18-full`

```console
$ docker pull amazoncorretto@sha256:9dcef4ef92dc11b31a61cdfe6f3cf72c30bfbb6c7183df734e693da1a1e4c3f9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18-full` - linux; amd64

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
		Last Modified: Fri, 14 Feb 2025 14:36:09 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a00dafba695643a64ad97c0b5be7979ea4effbf199f23b1a9eb9f8862c8449bd`  
		Last Modified: Thu, 08 May 2025 17:05:00 GMT  
		Size: 159.0 MB (159032821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-full` - unknown; unknown

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

### `amazoncorretto:21-alpine3.18-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0fd98454e44b437fb28f9eb3a848eecb5c512877415d23689bf32d433e6b3cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160340410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c66d529ce3496c34302fe076c0a0eca7c38be3c71f0667e590e6c9a6bcfd1b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:03:06 GMT
ADD alpine-minirootfs-3.18.12-aarch64.tar.gz / # buildkit
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
	-	`sha256:95459497489f07b9d71d294c852a09f9bbf1af51bb35db752a31f6f48935e293`  
		Last Modified: Fri, 14 Feb 2025 14:36:47 GMT  
		Size: 3.3 MB (3342657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaf0c34f21553fde282ad88a24dbf690c69d5d2014cb05b32a435a3c581a302`  
		Last Modified: Wed, 16 Apr 2025 00:18:59 GMT  
		Size: 157.0 MB (156997753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:384ced119aba4881216256ad0ae2af1f3d96475332dacaf6e66552fdc64da15b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.1 KB (389066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c2db8a7ef677140feb1a81d480536face96a2947b0f7c6097b9662bdea8652f`

```dockerfile
```

-	Layers:
	-	`sha256:77b8036688dd72a8e436d1bee292c55dda5314fee155c8ab414a62b09c45d2c8`  
		Last Modified: Wed, 16 Apr 2025 00:18:55 GMT  
		Size: 379.6 KB (379550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63c13dac3fc8852ca402555d8d7d8a2bff3700bb90b0c69a91d731cb2ae2c6c3`  
		Last Modified: Wed, 16 Apr 2025 00:18:55 GMT  
		Size: 9.5 KB (9516 bytes)  
		MIME: application/vnd.in-toto+json
