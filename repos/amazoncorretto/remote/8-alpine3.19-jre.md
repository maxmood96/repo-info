## `amazoncorretto:8-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:bfd567c00168775178e2bdd76a22779867b0f3b952af3a4ea5c42a1290f5be89
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:092681c4b6fe0f21726db6aae0a6f0db4c3583faa0b5a15fe13f2e057bf9de8e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45068851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60cc9fcb41f8635b51da9b720b84b1c9f2e630c28dddc1d36f73b0d819f3e856`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1b208ea6077e70a7d01694e7975a332710f838ecb54be09b37c4d323a14437a`  
		Last Modified: Tue, 07 Jan 2025 03:28:23 GMT  
		Size: 41.7 MB (41655580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:920953ed3ce91b7f062ba5e86f8ec0b81538e8c38d72828a34444b85ace5a37e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 KB (194030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6927f13dcfc7261791759203cb01d9cc562b41d21e4516af93732f4a4b26b13`

```dockerfile
```

-	Layers:
	-	`sha256:a7245b325aa938bb049f34a9aac00e3d13266b6c29926e9473817ab60a9c9c75`  
		Size: 185.3 KB (185331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:916e8821b3bb70b5051e63457bbc0cf2c66ec15f390e420c38389115c8dbe0b9`  
		Last Modified: Tue, 07 Jan 2025 03:28:22 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:edef0e57f386fb7d9df492b8638917021183a22d9576aed0fecd192f7ac4f4d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44717868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a60a39d7b2bb79797dceb726c1b54fb04ceac069c0967c8ba66ab513cabec9ff`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=8.432.06.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6314e88326c340b55228a82c51d2d830219ced296baa860450d2ecb18463670`  
		Size: 41.4 MB (41358622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:abf7d20cffe459760f74a1bc85eea1922364168661d5aa8b1ece9d21a4f5fef4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 KB (194411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37f99aff23b32509b474af90da67a5f7c6bf740b3a468c92c47287c03ad822ca`

```dockerfile
```

-	Layers:
	-	`sha256:4b12c3f05fd01adf85550dac6f25b5eb76774ae9d870bc1eec8cd6e8e32b01ea`  
		Last Modified: Tue, 12 Nov 2024 11:04:56 GMT  
		Size: 185.6 KB (185632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a36d0015049241d448774ab4315ed812849e7c38605739057fcf01b9cf51df73`  
		Last Modified: Tue, 12 Nov 2024 11:04:56 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
