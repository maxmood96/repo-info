## `amazoncorretto:8-alpine3.20-jre`

```console
$ docker pull amazoncorretto@sha256:4c2dd8ddfd1a7cc414c0f70232ecf0f7a04d644c2b69eb726f024d6deabff3b8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.20-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:86ef3a261cd704315e581baeb6033ace1b906593c397173f5838d7bc30acfb8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45357707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09444bd15615fc3712e95dac616fa3cd3417ed5692c599ce51dc4a3d28a509ce`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:5311e7f182d02360a7194aa2995849bcdf04795c39a0ffdcf413eae625865970`  
		Last Modified: Wed, 08 Oct 2025 12:03:10 GMT  
		Size: 3.6 MB (3627056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5b73ab11a329311e4d1ead18e798c4ddc25abba5b5a8762d0f7529b11435183`  
		Last Modified: Wed, 08 Oct 2025 22:59:07 GMT  
		Size: 41.7 MB (41730651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:61bccdd3b5b4dfa4b324d735618e12afff5aa3574bcd8a81974f52ae63e5f332
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 KB (191393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73a21ce2e153693cd315598b9b00cb49b3c01c82b5ba55fce1af8d48a3ed7b9b`

```dockerfile
```

-	Layers:
	-	`sha256:7d14690f62cfa42c4e0fbb04c6af44d6dd8850bf812695deba030070a5267795`  
		Last Modified: Thu, 09 Oct 2025 00:53:39 GMT  
		Size: 182.7 KB (182694 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b105efde696e7b951508e68043eafce5c70f1d6aceb52b0bda7b67e38ff18ab`  
		Last Modified: Thu, 09 Oct 2025 00:53:39 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.20-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5a2f2c15e6ffaaeeec24dbe789f2c26d3a0c1121e5258cf7d3d5d840762eeb05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45526123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8867455008004220581d5fe30ff891f481aa429e10209cdccab657c312d1756`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.20.8-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:c765ae84869fd59a62821873e5413a3e92e36bdc1ced8fab3520334863720a49`  
		Last Modified: Wed, 08 Oct 2025 12:03:09 GMT  
		Size: 4.1 MB (4089377 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dbded0e2f6f0f94ca85168f0f452f2cc58095706b8330e0584f561a508c17be`  
		Last Modified: Wed, 08 Oct 2025 21:46:26 GMT  
		Size: 41.4 MB (41436746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.20-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5a9900c42995719be603bfc81fce56e375f92678861a79eaa536ccf294e76a8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.6 KB (191581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07cf6573cf8321dc55cd1637f73e7d3900752a901c4f9cf7d13e01c14ef16da`

```dockerfile
```

-	Layers:
	-	`sha256:4c12fd2b87d920e9662f543c22c4db8d6fe8eecd657211731182aff294235903`  
		Last Modified: Thu, 09 Oct 2025 00:53:43 GMT  
		Size: 182.8 KB (182802 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3546e2a7f58f7f0a6a8d4f505df4a7f9f90a41bd9e41a11f69d38e223028a0a7`  
		Last Modified: Thu, 09 Oct 2025 00:53:44 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
