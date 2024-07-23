## `amazoncorretto:22-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:c99da242fc79afc801178faa50d58ddc3bdd21ad418e204f0fcaec083c48e78b
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
$ docker pull amazoncorretto@sha256:d665f7c6abe0a12d0ec49dd30be5ad8751eb18cec6f1f1de2294176f52303049
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.5 MB (158467266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfcee4f45343320dc6bead0aa913acece5945027d18437dca69d81dbf2589d94`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 20 Jun 2024 17:40:45 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Thu, 20 Jun 2024 17:40:45 GMT
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
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:957a16b128ba58cf230a0e70f29d0a33401028ae10c834f84cf7fdd9a2589ee2`  
		Last Modified: Thu, 18 Jul 2024 01:28:46 GMT  
		Size: 155.2 MB (155194680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.17-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8f1614c9d74094fd0f3450dd1d077403cf0eb87c0b9046a80f9a87e90fd020cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **388.9 KB (388890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67ceff0d327c6777c5093b1b17efd8b8c871c8b56da86ebb3d9c6a4380e5a87`

```dockerfile
```

-	Layers:
	-	`sha256:c8bc20bbee15c29504dc9ca270205420381354b0f1a29622ecb36c798a2ce0e3`  
		Last Modified: Thu, 18 Jul 2024 01:28:38 GMT  
		Size: 379.4 KB (379421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39ecc84bbedeea410dc7d4670efea5a671c704090a510e20932929e791c1f7f1`  
		Last Modified: Thu, 18 Jul 2024 01:28:38 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
