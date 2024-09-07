## `amazoncorretto:8u422-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:5ce46c449ecdb3734aa12f078e3c73885c9f9fe96919e23c436f5c94ee136d74
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a0f4de17e7c50843155526926e39fbfac66a88f7b680b080caa719f921844dcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45223463 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925e8d26572d963d372a738be767819975116072f18e99142325d0161f6fb8c8`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd37011fa32788b39c2537127eb1bbcad8841d25b8c05537c3fbc875eb858049`  
		Last Modified: Fri, 06 Sep 2024 23:16:54 GMT  
		Size: 41.6 MB (41599656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8a80d3f6046caecd271084b3679e3fd64375b7b79f95534efe7385a891b713bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **190.9 KB (190925 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98865fb75e9f4c9fd2d6f64d3f0d9790fb4d97cb6193818bb8ea26be867c14e5`

```dockerfile
```

-	Layers:
	-	`sha256:6bf24ddb58b81e597d969192d55c1e71664053ebe80e51285341d33c78bbd6e6`  
		Last Modified: Fri, 06 Sep 2024 23:16:53 GMT  
		Size: 181.8 KB (181811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:170e4aac9c53b81e236f0f0877ae83e3a43f8f9b7830f3035cedd9c0a1d3e252`  
		Last Modified: Fri, 06 Sep 2024 23:16:53 GMT  
		Size: 9.1 KB (9114 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u422-alpine-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:7893b3fd7f39e99160dcccdbead6ea49ab1ae99e6d634afff57eee5665d259d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45393001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8687f445814a0c39b9cf913c2cc492b51b2736fb74c0a410d2eb28a1b5429e79`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:a71f7e9bc66668361f88637c724c44deeb2774ec268ff0a68bd99014c8a02a84 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:690e87867337b8441990047e169b892933e9006bdbcbed52ab7a356945477a4d`  
		Last Modified: Mon, 22 Jul 2024 21:44:38 GMT  
		Size: 4.1 MB (4086934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17277bbeb2222bb58f548ed656a91bb4ad3615ea5cacec81efe0091045e090cd`  
		Last Modified: Wed, 24 Jul 2024 16:29:55 GMT  
		Size: 41.3 MB (41306067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:9e0e218fbacab07aa92e25cd946e8f989b2cc7d2876e8e3bf44f87459e8ec23e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **191.4 KB (191357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8466f36c4d0a4e01ab29fdb77cddb5191ca72e59a8bb1163c9001ce29468f13`

```dockerfile
```

-	Layers:
	-	`sha256:f2afb5645dcd7a52f567f09029dcca20632b7e935de409e8fd9e8fbcfe206cb2`  
		Last Modified: Wed, 24 Jul 2024 16:29:53 GMT  
		Size: 181.9 KB (181943 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f2842dea1bc50f19e83f0ead892d646eeb858f3fc2bcc0b5c84c46e50d09dce`  
		Last Modified: Wed, 24 Jul 2024 16:29:53 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json
