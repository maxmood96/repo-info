## `amazoncorretto:8-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:a8dd7339b74586a42a5495ec7d3ecc27831478b65900aedebf4b29d65931db1f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2a71a31baebf6b6d314d55a4cd0a4b0c4bf4fb64f4df2d34206d8a259a33d34b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103610380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2270c28827b2b475a126b07ff22cafc8dc2b2a34022edf7c20452875209a039f`
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
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 13 Dec 2024 23:01:14 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:eb002c13a70b63d5677b5a03f11b7b8b60f7d62f296fbb7475169a617500d3cb`  
		Last Modified: Tue, 07 Jan 2025 02:28:43 GMT  
		Size: 3.4 MB (3413271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b3952ef33cb0738a9cbfd179010cc53538d57caede38249d725cdd2a241f2b8`  
		Last Modified: Tue, 07 Jan 2025 03:16:02 GMT  
		Size: 100.2 MB (100197109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eef69312c96adc5971074f4a42a5b8d6105fa47039dfecd7b9d5f1bf0fa6e420
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.0 KB (255030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b54524d79b466aa621a243c738f737d552dbce3701b4a7039b7325a5b1e762d7`

```dockerfile
```

-	Layers:
	-	`sha256:12b0a50c6950479514b96ac5899f064d00cb6d0bc2eb076b9198ce113a9f2c04`  
		Last Modified: Tue, 07 Jan 2025 03:16:00 GMT  
		Size: 245.6 KB (245632 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93121e51a352a7bfb51c45bb4acd3ea248763d02682c2af60a7e1854f6936622`  
		Last Modified: Tue, 07 Jan 2025 03:15:59 GMT  
		Size: 9.4 KB (9398 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7ece8adbb1c1f9c4ab4de0c9e02d78677a6a56495fa4e56af43258dd39734330
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.3 MB (103338324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afada319287cd7b5d29c12f469c2f9e929577a4f0c3e1f176467f92b7182e5fe`
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
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 16 Oct 2024 02:18:03 GMT
ENV LANG=C.UTF-8
# Wed, 16 Oct 2024 02:18:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 16 Oct 2024 02:18:03 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6c9d4d66fb4987fcd48c673e8b29bb504a3cfb33f10b97cbcea126aa3b8b59fd`  
		Last Modified: Mon, 09 Sep 2024 07:03:21 GMT  
		Size: 3.4 MB (3359246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8eee8cc96a9553912c158db877ef4d5c02d81833d0c47cb76cfba118e08ccc`  
		Last Modified: Tue, 12 Nov 2024 11:04:18 GMT  
		Size: 100.0 MB (99979078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f6c4fb8147fe7a6172563c6ad2d5302827fc75d28535daba8096f79be8863dd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.5 KB (255518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cea4d3a4866d70f6ce52664c962f8cadf3fb568ba85d791e39550c7f5b2b4d9e`

```dockerfile
```

-	Layers:
	-	`sha256:22e2cfdec280411ab640c8854f0f26d01f2093e0c03e1f77d539909588346749`  
		Last Modified: Tue, 12 Nov 2024 11:04:16 GMT  
		Size: 246.0 KB (246017 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49a95c6295cef24fa781487c80385efe636be2d01d45d959912dcbb5b0d377a9`  
		Last Modified: Tue, 12 Nov 2024 11:04:15 GMT  
		Size: 9.5 KB (9501 bytes)  
		MIME: application/vnd.in-toto+json
