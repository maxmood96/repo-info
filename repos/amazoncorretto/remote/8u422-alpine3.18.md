## `amazoncorretto:8u422-alpine3.18`

```console
$ docker pull amazoncorretto@sha256:9bd4d2ffea9d0da28249e68f616799283972403335c370a560b4c7309004b6f3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.18` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:76d56c0616d5940859d242357a7a421b26d4d8eaefe5babfac5fdf0c9fc4c941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.5 MB (103539380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c403c0e785e22ca87c8930fd308b1e84854022d90738bd00d983c447b1ca6032`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5851aef23205a072ef361dd412a73a39a1ada75e19a207a392bb7ec9b8556e11 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:930bdd4d222e2e63c22bd9e88d29b3c5ddd3d8a9d8fb93cf8324f4e7b9577cfb`  
		Last Modified: Mon, 22 Jul 2024 22:27:34 GMT  
		Size: 3.4 MB (3415640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8990b85602c9da3cabeb1d1f5ce449a184f9e5c23a1a35cabb12e0af22367d8b`  
		Last Modified: Mon, 22 Jul 2024 23:04:28 GMT  
		Size: 100.1 MB (100123740 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:530a6b52f98dab20964d3ede202cf302d7d0e31b60b5d3ae9989d170632e57e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.2 KB (254228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16c5980b47c1d2fae16abbc5c2ff1d8898f4003c9e23f4ddc41d3210eea28ae2`

```dockerfile
```

-	Layers:
	-	`sha256:85909688b4e7f2505d835fd22cbf510e72870ff43b992624af8f05c67ed079e6`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 245.1 KB (245075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:523e21ebacbb9bc3a69b12fadd9ee1c581b9bdaee77b7dab066a60cc9020fcdc`  
		Last Modified: Mon, 22 Jul 2024 23:04:25 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:42c5a9e76b39430e760513a27bd58a51365cdfea78746da76c1a3848356bbaac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.2 MB (103175425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b82c04d1a356d80a6f5261deee66c6d70edf8da49466694ca3872c74597cca9b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Jul 2024 22:56:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:439e6a3a58b098e98be3c67c1056b1ad0f5c908e17ca369d0ccdea4d2f6b1d3a`  
		Last Modified: Wed, 24 Jul 2024 10:37:46 GMT  
		Size: 99.8 MB (99835931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.18` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3e3c475f7031c92307ba752878258ee8671b7f3dcc42ebb505b29b5f1638abdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **254.7 KB (254659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdff50760433a0d3ab5d8c987f065992d86532c6b47ee803f89c79dd1ba8b392`

```dockerfile
```

-	Layers:
	-	`sha256:81ed5cd809be495b1f697b374e52b976365a45d6e29822a7576b82dd240d1056`  
		Last Modified: Wed, 24 Jul 2024 10:37:44 GMT  
		Size: 245.2 KB (245207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7010a7ddb8977ea2560d39fe16105b8afcb4bbbd59333061e326b1bdd9f728d3`  
		Last Modified: Wed, 24 Jul 2024 10:37:43 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
