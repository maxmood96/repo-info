## `amazoncorretto:11-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:00b1db00c156aa5ddd0bfadbf7701a1065dc7dc40613e53712895348e8eccc21
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5b11c7e8ebdeba9f2eb23dc9f4fa6cc31776717ae3dccfcf3b51e95bf80d4f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.4 MB (145367106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:705e3dc226878539fd2ff162def67231c5782576ba53ae24300f5c46c4947bde`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff7144c9cf698c00afafad75bdaf4617f3c891b1f7fbf2d945e6f513bd5cfeb`  
		Last Modified: Thu, 08 May 2025 18:00:28 GMT  
		Size: 141.9 MB (141946238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:14eee702cc177e797a7cfc8286d47eaf6b28f1d3fb6d91150bc93e3f50dd633d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.1 KB (397110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06491ce1d5cf847081a0c922c76646f17ea867664a3319f934693387e8b7c5c4`

```dockerfile
```

-	Layers:
	-	`sha256:69d5b5ebb01cf77885196e0b8bc8b3e588a127b6cc12b5b115115db130758223`  
		Last Modified: Tue, 15 Apr 2025 23:55:30 GMT  
		Size: 387.7 KB (387693 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bee05b953a1cb8c2006c380d175d3f9486594b68245b0946dda19ffebe1b0ec8`  
		Last Modified: Tue, 15 Apr 2025 23:55:30 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a8f7b790b0055cfb8c8df188b136a8b5f90b899d627ff37de24bef935066f213
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143429328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da180d2b7cc3d62970c82f833615229ee0179df2bd0d0dfe236d3946c44c853`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=11.0.27.6.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=11.0.27.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Tue, 15 Apr 2025 21:50:45 GMT
ENV LANG=C.UTF-8
# Tue, 15 Apr 2025 21:50:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 15 Apr 2025 21:50:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 14:31:17 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e609d776b9d6d42ee1f23481a668189ad05a9545e1a27c136e8bc95798a65a99`  
		Last Modified: Wed, 16 Apr 2025 00:06:28 GMT  
		Size: 140.1 MB (140067904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a84fa46f1b4b29ae56da37cfeafa58d7553d860178f2e6d9f16d07d8eafd5593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 KB (397270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6645d7c2f304e03323d1a6c8c022fb0bc9de1ae8fd174db07145e8ceff8d1727`

```dockerfile
```

-	Layers:
	-	`sha256:1da5c7179a5d61c545b2d555c434e8cc973a6e457e9da4166da0a8f7344b08c4`  
		Last Modified: Wed, 16 Apr 2025 00:06:24 GMT  
		Size: 387.7 KB (387749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0ec57e1bfc9bcb4a60f02e5ba9b0b49a36e02e7076f56a287e3faddba7b9eb`  
		Last Modified: Wed, 16 Apr 2025 00:06:24 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
