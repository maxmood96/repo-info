## `amazoncorretto:24-alpine3.19`

```console
$ docker pull amazoncorretto@sha256:2234647fc02d3c87554d0f2455672bba942e0d9c210b8d9736e6627370041436
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.19` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6557cdb5d545e1d224d002a6a483cea3bde6e8906b25f88a383f35bd3141a33b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180024964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74141733f9e2f6e103beaedca15df1d0a1b0aba59c25ee3a0653ccc0d05bcb4a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Tue, 15 Apr 2025 21:50:45 GMT
ARG version=24.0.1.9.1
# Tue, 15 Apr 2025 21:50:45 GMT
# ARGS: version=24.0.1.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:4bc235731fa69d232d460559bfdc28bf050b8e1482d61f14f30f4bab1beb8cc7`  
		Last Modified: Tue, 15 Apr 2025 23:56:05 GMT  
		Size: 176.6 MB (176604096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1b8c649b6642361ee91278f97ca64001788eefd0592cd59e422ef6ed26f4e2c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 KB (399296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e223bd2337c5993af85d531ca06088c555df679c306d0d8ef7b520288a1e1e6c`

```dockerfile
```

-	Layers:
	-	`sha256:3ca89f2dce50fe0f156c2e368f763608fb730ad7035c5640e9c7a44786c8fbec`  
		Last Modified: Tue, 15 Apr 2025 23:56:02 GMT  
		Size: 389.9 KB (389882 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:548d2dc2958f66ee9d1afc141ca5b8dc7725c405de0db97288436cab958030a0`  
		Last Modified: Tue, 15 Apr 2025 23:56:02 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:80b7e36b69a4b481874a4b37fb1431805a818679845ab2c3d78e956764e7a0b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **177.7 MB (177658249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6d326ad72a40f7fb5ee1b233133710c3bcccf8f81e90532ce3fc11c0718048a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:05:02 GMT
CMD ["/bin/sh"]
# Fri, 21 Mar 2025 22:11:14 GMT
ARG version=24.0.0.36.2
# Fri, 21 Mar 2025 22:11:14 GMT
# ARGS: version=24.0.0.36.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-24=$version-r0 &&     rm -rf /usr/lib/jvm/java-24-amazon-corretto/lib/src.zip # buildkit
# Fri, 21 Mar 2025 22:11:14 GMT
ENV LANG=C.UTF-8
# Fri, 21 Mar 2025 22:11:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 21 Mar 2025 22:11:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d13a3fff434d56c3504596695435266be8d07061a80359aa09366eea2e094aa0`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3361424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ee10e8babc5161b1900d75aff9366c91bff23cdccdc40684f3ca464d14eb0f`  
		Last Modified: Mon, 24 Mar 2025 17:36:28 GMT  
		Size: 174.3 MB (174296825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.19` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:22d1f740a8b185c52f568d48aee62cafc4a6d9e1e6a57432b23953d1fa2b1ae8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.8 KB (398811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f70a8604b8c5db6a4ae686a9f8c18b1ac17e2b7a20dbcaa1ad42b6bf46ff89`

```dockerfile
```

-	Layers:
	-	`sha256:6001f60f699b42041e93c05b317cb9f556257e7fc4ff1fe18689c854d77351d6`  
		Last Modified: Mon, 24 Mar 2025 17:36:24 GMT  
		Size: 389.3 KB (389292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cc35623fcb498ae9a45572a302489a7048839c4e0f0e0fcc85d58ec0a47d4d`  
		Last Modified: Mon, 24 Mar 2025 17:36:24 GMT  
		Size: 9.5 KB (9519 bytes)  
		MIME: application/vnd.in-toto+json
