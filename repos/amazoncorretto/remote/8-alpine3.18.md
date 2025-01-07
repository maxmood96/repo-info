## `amazoncorretto:8-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:d02d9a83a23faec2213e33d8f1dfb66069b49d059e7993391c486c84e2c19c91
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7ae5658ac6918c5e494b08ddb67934de51b70905a411379501af31c008e1b82c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103604332 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f1cdfef3f699083ffd09c98793316c8b35154ead5db3d342ea8ac4de9c750d6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.18.10-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5fa62e1bbddf13eb6443e20aa8ed938bec91a8a5d5d0a26e58e8eafb3ada9a1c`  
		Last Modified: Tue, 07 Jan 2025 02:28:37 GMT  
		Size: 3.4 MB (3407632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7397b3fabdaac0245a0b59d564ae8050fcdaaa978ba680fe21fc5ac8075e4649`  
		Last Modified: Tue, 07 Jan 2025 03:15:46 GMT  
		Size: 100.2 MB (100196700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:20219b281b9fca40bc8c7d2f2a10303668bd0cb99c2b2177d36a2fd1cf28c98e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.4 KB (254371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b47c07feb5368d66b013730c68883aba61cacc024dbd22e645ea8028219acf4`

```dockerfile
```

-	Layers:
	-	`sha256:dbc14b62707eb09728dad9460b047c37e4ef86034b2dc992bc66400a4be30259`  
		Last Modified: Tue, 07 Jan 2025 03:15:45 GMT  
		Size: 245.0 KB (244973 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:29508cd66404ca0248d74b1e5e2f28d959a56f445f5fe402e1cad979be8f1a1d`  
		Last Modified: Tue, 07 Jan 2025 03:15:45 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:925801aa95a0a81e7a188f4c45b9b7b7661aa68d11a054f2bd74bfcce5349ee5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103319577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:236840f530698a2adc7add2850459a36c9e7d0b3340fbc1458920f63bcf6b5f2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:03:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:0dfcae9cb3f09031e3687535f2d3e3c2f08533799b67ed61076e79e4ed1c7c4a`  
		Last Modified: Mon, 09 Sep 2024 07:02:44 GMT  
		Size: 3.3 MB (3340451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3c3288aaff59afeb2d3f06934c671c5bfaf6c1f73c431aef825fa2a5aa01620`  
		Last Modified: Tue, 12 Nov 2024 11:03:23 GMT  
		Size: 100.0 MB (99979126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:263dc6652835be3c7091bff58e978fae7eb8be3450986aa6c7661b3d2f294be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.9 KB (254858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaa17a86f3f4878cbd5862582e58bebd8f5b58492f6b586263a0fe9f0e95d100`

```dockerfile
```

-	Layers:
	-	`sha256:d3285f00738be2c898449a581f905cd74ae9d42c399f8a4193ad0452887332e6`  
		Last Modified: Tue, 12 Nov 2024 11:03:20 GMT  
		Size: 245.4 KB (245357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4480ce776ad8816e2904f7ffc6e578f6197c6dd7604846de8b9d3f59e302cd7`  
		Last Modified: Tue, 12 Nov 2024 11:03:20 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json
