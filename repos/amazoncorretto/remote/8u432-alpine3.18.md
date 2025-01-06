## `amazoncorretto:8u432-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:f5cc0f0f0f24c48100bacb8254cdb880a57947281c77f58e401a156f126dad5e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a88a4f859ba2e9a758c32be45e6d650e9221b6ea870f415d5d431d8c6d5f2da0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103612874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac38c35d6f1fc1cf4c61ca3c4b3c86911c52b01d053f8e41673caa1444bc9d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:03:22 GMT
ADD alpine-minirootfs-3.18.9-x86_64.tar.gz / # buildkit
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
	-	`sha256:dc0decf4841d19b14e836c2d82bd5cb9540fb5e0d1359549ca243f49036557e9`  
		Last Modified: Mon, 09 Sep 2024 07:02:43 GMT  
		Size: 3.4 MB (3416401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eaafd4ec1bf4522763df921d5b3ee7587400d37884c29c4bef96dd81f23b4d1`  
		Last Modified: Tue, 12 Nov 2024 02:11:53 GMT  
		Size: 100.2 MB (100196473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:472608f0e4f41db29b825e81202b1aebd804f7a62ad1fe3b0a6d883b13ec3a76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.6 KB (254623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:934f9acdea9a8c1a53f6c3d41f64b69996115aff8a4ffc74a6e7b1b96fec8227`

```dockerfile
```

-	Layers:
	-	`sha256:96d07eb74c6daf76f5d3cbcdf4dfe248a20a2048adb6c39f78e14aca312e47e6`  
		Last Modified: Tue, 12 Nov 2024 02:11:50 GMT  
		Size: 245.2 KB (245225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:677546672e5fa1c036cb1f35450930bc1a761420e4462024bfa7e809db194c3c`  
		Last Modified: Tue, 12 Nov 2024 02:11:50 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u432-alpine3.18` - linux; arm64 variant v8

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

### `amazoncorretto:8u432-alpine3.18` - unknown; unknown

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
		Size: 245.4 KB (245357 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4480ce776ad8816e2904f7ffc6e578f6197c6dd7604846de8b9d3f59e302cd7`  
		Last Modified: Tue, 12 Nov 2024 11:03:20 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json
