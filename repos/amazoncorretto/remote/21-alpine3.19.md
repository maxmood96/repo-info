## `amazoncorretto:21-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:848d95b489d89a9659307c9c3e4a3ef8e50466f83e05720a3fd79a4b76013f73
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5f84f8374758f707021e153b7d892acd3c28e5a58b2952faefe120f00a10e7ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.0 MB (164986606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6a90accdcfca5a220a4e373e1027209055380118fd164a53b8c18537eddbaed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b51528d40984545fc6adcac67d25d4f3c1750de4243649ca11bbaa90714ac17`  
		Last Modified: Wed, 22 Oct 2025 00:56:26 GMT  
		Size: 161.6 MB (161566791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d9b648061d7a8a715827911ff0d848ccc487cc8554ba434c67f9a43c29565a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.4 KB (594370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbc15e60977bdf60859803d8923545307f8bf1bc19af87f1a924a5f13975f1f6`

```dockerfile
```

-	Layers:
	-	`sha256:257cff0512e9b6771014b923f4e4d5ee9c6e745e5f7067139578a0da9b4b2ce9`  
		Last Modified: Wed, 22 Oct 2025 00:52:15 GMT  
		Size: 585.0 KB (584955 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4baf8b578ff2922aa1037b5c48b152ea48931bc19a00a9a58e008693b399ec50`  
		Last Modified: Wed, 22 Oct 2025 00:52:16 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bf3ff6e98e9642c2685821ed9fe332d8ccfa1d78ceb6319652d657595ae6e500
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.0 MB (162956906 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b97fc26ddf68bc485bbb601e450be36a23f0a20bdd60fcbeaa9cd988ea33539`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Oct 2025 11:10:40 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:10:40 GMT
CMD ["/bin/sh"]
# Tue, 21 Oct 2025 20:48:19 GMT
ARG version=21.0.9.10.1
# Tue, 21 Oct 2025 20:48:19 GMT
# ARGS: version=21.0.9.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Tue, 21 Oct 2025 20:48:19 GMT
ENV LANG=C.UTF-8
# Tue, 21 Oct 2025 20:48:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 21 Oct 2025 20:48:19 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21860f3a40972016dde996e0adc21e63f7bc7e2c91b1210e9949b6b96a58042a`  
		Last Modified: Wed, 22 Oct 2025 03:32:27 GMT  
		Size: 159.6 MB (159597605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:3acf190347b39ba1384191423cc0312f9155e88b1380c65a925d7bf7ab77d08a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.9 KB (593893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b2fa7fef4ec801916dd176e66dfe4183eb433435930b77a97dcc7a0a87385b3`

```dockerfile
```

-	Layers:
	-	`sha256:5e2aa8f584481ed11d901b736bc5a156abaad8c12e057398937c8da157744d85`  
		Last Modified: Wed, 22 Oct 2025 00:52:19 GMT  
		Size: 584.4 KB (584374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da2db86ffc5adc035bd7509c12b0c7254460c6d1a147ec228f0408d43ed6c6ab`  
		Last Modified: Wed, 22 Oct 2025 00:52:20 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
