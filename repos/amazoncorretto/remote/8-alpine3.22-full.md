## `amazoncorretto:8-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:70e8638960d212ed2e81cdbcbaed13a9834a2e44faabf309fcd834827b65bd6d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:70616869175fd05d5235e46c4570968f694b4f4b096dfd94ca88281ec11d94f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.6 MB (104560337 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef224fbb36bcb2dcca2a41db2bbac1ff882a8be3f90aab2059703631eecb3e5b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a92574770f6746e0040e247649931c248a47ee8d6ac55cf021609a6a99672a25`  
		Last Modified: Tue, 21 Oct 2025 23:26:15 GMT  
		Size: 100.8 MB (100757885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b07b4fd76b2a1844945c6dd59da143bd5130db840ef114a0d2c5d617e41265dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 KB (259668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f316032f84c4f7ec9c3337cb58c2cf106d2b7ef73b3442affa95c0a8e7bbcb2`

```dockerfile
```

-	Layers:
	-	`sha256:14a21cb4e067f0b07b8c8f76a76225777c4933a0297fe0f721b911b46c7fe607`  
		Last Modified: Tue, 21 Oct 2025 23:26:12 GMT  
		Size: 249.0 KB (248972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c728148039ecd9f9ba074e1cdcf31787faeb06ed7c621c15a6041399879b024e`  
		Last Modified: Mon, 22 Dec 2025 08:22:45 GMT  
		Size: 10.7 KB (10696 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:805005c29a698fa407339507d907b57c778806ba29fabaaa690a74763f620ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **104.7 MB (104671366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce0328a55911998b0283aec1daf3927b4cc310eac2faee7d590aae9c8b26641a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=8.472.08.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=8.472.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2744539f18ab260f7f42fe25f3c1d2ed1c04d685e18106e294c21f0dc1975c3f`  
		Last Modified: Tue, 21 Oct 2025 21:49:01 GMT  
		Size: 100.5 MB (100533297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:df1986ae49f5a137b403a7f6bf8b551f2677d44f782d6741bce85bfad73c2eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **260.0 KB (260000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129d4db6839af2013b85b179c64968a5256368c1e07abf7a2f74e0966555e12e`

```dockerfile
```

-	Layers:
	-	`sha256:cac6d7e3ea6c5f31ecadb579017024860527406818278efd9bcecbb9d98949a9`  
		Last Modified: Mon, 22 Dec 2025 03:04:48 GMT  
		Size: 249.2 KB (249152 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d8a3049fa52c471e0fa3d7054ccb009b41cf3f2c9864cee9d40d72743c97c1`  
		Last Modified: Mon, 22 Dec 2025 03:04:47 GMT  
		Size: 10.8 KB (10848 bytes)  
		MIME: application/vnd.in-toto+json
