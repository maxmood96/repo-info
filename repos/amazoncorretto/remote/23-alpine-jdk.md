## `amazoncorretto:23-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:6d2a7b42ea97c88639b02852f6459f81289a1d9875b6cd6698a2c272aa0d6c94
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:23-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5e64cf1b2c1d6429c2535bf5b24a6929a43849706bfc3f01fe5b2c87c13169e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170263017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c7697dc41ce1083e6f6c56476fa515ea4589c25d3e5f688b2c0993ec4310a9c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37.1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Sep 2024 23:46:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990d85a3742dfcf24bdc9c22759db7f037b2b1fad3196124404cc028cc0eba60`  
		Last Modified: Fri, 20 Sep 2024 23:56:03 GMT  
		Size: 166.6 MB (166639210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:fb904d1af3dacbdeae83c681ff0c8afc018c46c45657c0f7a95b2824f46e1f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **14.2 KB (14163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3676c09e634dc6659aab63b7e4bf5c8c216635f8180c2a0effea854d4cace38`

```dockerfile
```

-	Layers:
	-	`sha256:3179f87a91399780d3a8a4c9d61458a6988bde3e369bfc393e29d60901a7c06d`  
		Last Modified: Fri, 20 Sep 2024 23:56:00 GMT  
		Size: 3.7 KB (3687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b859ba9ebf2df2c1d90332d22e2d9a18bc9106cdd984b3cfe377ab74dde87f87`  
		Last Modified: Fri, 20 Sep 2024 23:56:00 GMT  
		Size: 10.5 KB (10476 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:23-alpine-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4a2c0a96761fe331c27490a8a61fb2bf2431c076a82986f4d660c0d09538e28b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168401231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8201636aa67fcac9550fceffe05537b8cbf430ff6214bf3d75cadcf27f377c2a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 19 Sep 2024 23:46:25 GMT
ARG version=23.0.0.37.1
# Thu, 19 Sep 2024 23:46:25 GMT
# ARGS: version=23.0.0.37.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-23=$version-r0 &&     rm -rf /usr/lib/jvm/java-23-amazon-corretto/lib/src.zip # buildkit
# Thu, 19 Sep 2024 23:46:25 GMT
ENV LANG=C.UTF-8
# Thu, 19 Sep 2024 23:46:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 19 Sep 2024 23:46:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9883ebf1b4472b6548e68567db02883376888e0ea7692cf741cbe14972bc2ce6`  
		Last Modified: Sat, 21 Sep 2024 00:49:14 GMT  
		Size: 164.3 MB (164313585 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:23-alpine-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f964ac7b3d50c416e53077ee8a1d9d6224b140d790a2df3df0b1d06fc1e6ede1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.0 KB (389977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2968a05f8c6f0f8e5b5321a2ec3cd8a4e9a021c990b2136106b2e1269c5f0a1`

```dockerfile
```

-	Layers:
	-	`sha256:3a07771bfbb8a4f40fd3776f7c3abdf9509657588552c343cd91b28a78b577a9`  
		Last Modified: Sat, 21 Sep 2024 00:49:10 GMT  
		Size: 379.2 KB (379153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55d877bc03a8bec708233ed14a7f7b5a0280c9aeec5fc44fe97dc9bbd316f2c1`  
		Last Modified: Sat, 21 Sep 2024 00:49:10 GMT  
		Size: 10.8 KB (10824 bytes)  
		MIME: application/vnd.in-toto+json
