## `amazoncorretto:24-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:cd3d9c7e73c6b8cc7695b8195413f29b751c0fef69dc1f74e9754f4ae757b04b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:24-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1229ae0cab299701cd06eb01a7494c51ee7e1d1b88a920b47601828b2753a06b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **180.0 MB (180030604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdfc44b80d36ec97e7c25f6fecf099c2d54f6aaf03d750f1440ad33ebd1d7463`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 14 Feb 2025 03:05:02 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
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
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 12:02:26 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5717dc16ebe1d5f515c4535a221fc28bffc276be0bec8f0798dbf9af63c3d74a`  
		Last Modified: Mon, 24 Mar 2025 17:04:01 GMT  
		Size: 176.6 MB (176609736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:24-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:18b11a0751f6579e2f02f800c58d80f456dd777165e3c31fa5d2ffa8140def4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **399.3 KB (399291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c35447abb9bfe3faf49922af7386477a9453620b0fa56a383ab0df0582c83143`

```dockerfile
```

-	Layers:
	-	`sha256:d3245a8b4fca0e5f1feee98e3ca93b9343a210af6adc65555ab539afdf6286c6`  
		Last Modified: Mon, 24 Mar 2025 17:03:59 GMT  
		Size: 389.9 KB (389876 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:33f15d5c05c81663dbbb5f6a3102e3e8e9d3fb21c982f5642a6346d43726ef74`  
		Last Modified: Mon, 24 Mar 2025 17:03:59 GMT  
		Size: 9.4 KB (9415 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:24-alpine3.19-jdk` - linux; arm64 variant v8

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

### `amazoncorretto:24-alpine3.19-jdk` - unknown; unknown

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
