## `amazoncorretto:11-alpine3.19-full`

```console
$ docker pull amazoncorretto@sha256:487f8c7a52a8a76bc97e80ba211b898284990ce42c925d62094003912ace424d
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
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dff7144c9cf698c00afafad75bdaf4617f3c891b1f7fbf2d945e6f513bd5cfeb`  
		Last Modified: Tue, 15 Apr 2025 23:55:32 GMT  
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
$ docker pull amazoncorretto@sha256:789b6e411c633467a6cacf0348f21adc24d6045ddaefb4d3a6c8f675f5784975
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.4 MB (143396400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd774cd93d7f1793924f31558e92d6311b1fefe12fe6ab25220dff421a0db1f6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=11.0.26.4.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=11.0.26.4.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:581df84a9c25e7bd30aac55b853e710ef9e5c8818170c6e1dbb8b44e7a75445b`  
		Last Modified: Fri, 14 Feb 2025 22:34:41 GMT  
		Size: 140.0 MB (140034976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ceff16f55e10c50ae9d0058a0937624208918b2e014738e97f70d9c6b002e008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **397.3 KB (397270 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a990411e9652e0b84d8c80b748ba862af0ad291755c6892c7f46959453d369d5`

```dockerfile
```

-	Layers:
	-	`sha256:6f037f7eb479bb0cbc3a2a09cdea4982f550bd126fb9f160e29d6f8bdc98a40d`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 387.7 KB (387749 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ca194cfe7d80a9aa47d8bae1edf6fa8f0f79543cee0c21f05d547a9e9648180`  
		Last Modified: Fri, 14 Feb 2025 22:34:37 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
