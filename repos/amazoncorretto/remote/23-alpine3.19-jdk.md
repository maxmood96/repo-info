## `amazoncorretto:23-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:82b7762a3253203f26bec8cd05024447773c85ebdff1f66655d76ec3f10e0844
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fb705274a9f25ba21db315b616318e3e5c9dfc9a35334dcf607b2bd7068a599a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.1 MB (170071882 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea08d6d1cb3e69289335bf045d7f49a8278a3c34bea529e8703ed74c953f2068`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=23.0.1.8.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:e366da9a439da668fe83eeae251fa112d3780c3d65c0364e66b324c20c55e5e9`  
		Last Modified: Tue, 07 Jan 2025 03:31:03 GMT  
		Size: 166.7 MB (166658611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:95f4953ebfb244fbc296fab8b10db12e25b01e5eeea75a0e481d030e9eaa0521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **392.2 KB (392151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d17d87f62f90f2425bf0710e9694ab1a6b7e8201622acedc21cadede65cd69`

```dockerfile
```

-	Layers:
	-	`sha256:6122324acdcd0ac09fc55a6deb7a2a3d5f6f2e91eb28d03bacb5488c5d093ff9`  
		Last Modified: Tue, 07 Jan 2025 03:31:00 GMT  
		Size: 382.7 KB (382737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b28e3d28080794c3cefc9d6c380815716cf632397d7f9a3ea7dccd31fb0be577`  
		Last Modified: Tue, 07 Jan 2025 03:31:00 GMT  
		Size: 9.4 KB (9414 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:e511832d9e7509cb40c0dbc6e9c753177ed09c1bc3760fcf65735a1fcb29cd9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.7 MB (167712322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bae4e372f2c90505ac4bb3413e09c46091a89457d434a919129acec8afedba7`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 12:04:22 GMT
ADD alpine-minirootfs-3.19.4-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:04:22 GMT
CMD ["/bin/sh"]
# Wed, 16 Oct 2024 02:18:03 GMT
ARG version=23.0.1.8.1
# Wed, 16 Oct 2024 02:18:03 GMT
# ARGS: version=23.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:3fbd0c45c6eea259598817c87ad8dc951eb824127bad36995733e93fef73fe33`  
		Last Modified: Tue, 12 Nov 2024 11:15:04 GMT  
		Size: 164.4 MB (164353076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:aca9bcd8ea8bd4a42f227557af22be9c45a6ccf8c6653ba23a9616f14080aa93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **391.7 KB (391664 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd6fab89ef40f09a267f4a16ce771c758c004c1c7ae66495537188f643c9a9e`

```dockerfile
```

-	Layers:
	-	`sha256:71afbd348deef6ba48dd99339178fabb3e917fc3db8292dc4f2cc023d50b15b7`  
		Last Modified: Tue, 12 Nov 2024 11:15:00 GMT  
		Size: 382.1 KB (382146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdce43b8728de939fb4749ef46e4e69fc698dbd911f6cce43d775de13dfd29c2`  
		Last Modified: Tue, 12 Nov 2024 11:15:00 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json
