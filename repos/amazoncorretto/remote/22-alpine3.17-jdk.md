## `amazoncorretto:22-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:235761953487b5462491117f47caf408072b2110efb73719c89959190962e163
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cd1c8fc7a9f61e1b2c1100219f4928fb02f8bd083e72fa43ed79c064ccddd11a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.0 MB (160988292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:343df81bfac0646aa326aff8a04160d3b78dfc1a7252732b414451adc7146dd9`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:ec892b6986dac395477ae6947272ea0913b711cda60bbd7d575b374ecfc4cee2 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:b99da37831f37d3f77de0ac7a864f9b69f1dbb4461e5ddfe5a3c2b7e2a3586c5`  
		Last Modified: Mon, 22 Jul 2024 22:27:42 GMT  
		Size: 3.4 MB (3391983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a94c320883cc982bded0b82487d5b370eb87ab9648536946a03aab0470c7d9`  
		Last Modified: Mon, 22 Jul 2024 23:06:44 GMT  
		Size: 157.6 MB (157596309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8f7219a55d54f8dc8757d17b8537c103d0775e68e44e9895aafb97736faf3550
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.8 KB (389812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86434f632a3b0a16d7f8bf3791a817e65161c2132835ac6a2d34e7c6dc3f794`

```dockerfile
```

-	Layers:
	-	`sha256:7cd01335acd7680123e8bfb147fdbf9d37f96b81c3feca0d735d9aa7a4dcbe87`  
		Last Modified: Mon, 22 Jul 2024 23:06:41 GMT  
		Size: 380.6 KB (380644 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c768084b4b2f3b3739440961c3585f1c03e701b317a417369f6a0a1eb5055737`  
		Last Modified: Mon, 22 Jul 2024 23:06:41 GMT  
		Size: 9.2 KB (9168 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:66bb320b05494ea19bdcca779e73808847d627b50f07c6a3474af10c2bc740f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158469115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9257eb18a017a7f9d31e3a5c3a3a7a06628686c16e2bd31ea233c0d9f1d43bd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:768e36150231c818b6707881e3060e9adfe496d4c48c00b59a05eecb16923c3d in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=22.0.2.9.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=22.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:dba698d60556788613e51a85af8ac1331430729add60c326c10517189222232c`  
		Last Modified: Mon, 22 Jul 2024 21:45:05 GMT  
		Size: 3.3 MB (3274245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7359796ec1e1b3ece216367679f0bd764dd2f049fc6a150ea888707c1d7844b`  
		Last Modified: Wed, 24 Jul 2024 10:46:56 GMT  
		Size: 155.2 MB (155194870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4e5d007a1be191b34465d9a435b40d039a496e060554adf8cd9fae6353894798
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 KB (388889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a9b05521b7739abb7200ff741afee8dae68e6c568b5e69d3626d5d97db323c6`

```dockerfile
```

-	Layers:
	-	`sha256:912d0bb82c9505ff203eb95eb3886a91c5aed73733fa4526c4667c69e60785d2`  
		Last Modified: Wed, 24 Jul 2024 10:46:52 GMT  
		Size: 379.4 KB (379421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:769e9b386ab5f5332565373dd70ecd6e879d2860e5b1fea7091c35090c8567c2`  
		Last Modified: Wed, 24 Jul 2024 10:46:52 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.in-toto+json
