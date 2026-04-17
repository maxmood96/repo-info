## `amazoncorretto:17-alpine3.22-full`

```console
$ docker pull amazoncorretto@sha256:ebc89fe856046319bba492b2c37e0bc216ec8300829c783c6bb6acee2e7f5136
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.22-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0908835aba7218afb3b054f21fcdc154148bf32a6ab7fa33bacea8209b0fe043
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152176806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5aee78e4a674aa0c823b5dcdfaf429cbb987a8816006dc93193a28ded7107fd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:43 GMT
ARG version=17.0.18.9.1
# Fri, 17 Apr 2026 00:22:43 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:43 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:22:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c575d0443bb0378e2cbb43f28e942299bef8a7fc0ccc411c06e17d82ddf0eaba`  
		Last Modified: Fri, 17 Apr 2026 00:23:02 GMT  
		Size: 148.4 MB (148368617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:490f51b28d19fd71cfc5065e11956c40fc4b61dfd51f5ba50c728717c9f14ff4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.5 KB (592510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a90f7babfbfabbac74860864bc01f5be6259de854301c48913c184fe2a158e`

```dockerfile
```

-	Layers:
	-	`sha256:3a4c059c3e74434dc5f652e0fd561fd90d187012d053291e78fd53501759532e`  
		Last Modified: Fri, 17 Apr 2026 00:22:56 GMT  
		Size: 583.1 KB (583136 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9b83fea9ad8b1625e9b4077866c0b4599816528854600a4837787d8ca1ede6e`  
		Last Modified: Fri, 17 Apr 2026 00:22:56 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.22-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:490c46267bed5104c1ea2ff4c0ccaf914cf9f68a34afec2273589dad4c98b078
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.9 MB (150855229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec843582cf003f28c65c07687e899247c9d158029c104ce91704fd16899e100`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:47 GMT
ARG version=17.0.18.9.1
# Fri, 17 Apr 2026 00:24:47 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:24:47 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:24:47 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:24:47 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4c36ce7263c49a6cadd2f786a0c693d5347a7809cce6f0ba16f73fb54e8502d`  
		Last Modified: Fri, 17 Apr 2026 00:25:05 GMT  
		Size: 146.7 MB (146713335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.22-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5c29f2dcbd45e6635b8dd8630c8b13ebeb5d72914e7c0b289619aa1e23749cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.0 KB (592033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45c1cb3fd7c84c87f89baa7172bbd89dc0925bb57c9dcd210023f8287a4a450e`

```dockerfile
```

-	Layers:
	-	`sha256:4591435c91ec611afd87dbc5ebef2400651efa19b6cec8a0481e8ba418428986`  
		Last Modified: Fri, 17 Apr 2026 00:25:02 GMT  
		Size: 582.6 KB (582555 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fa7c30e767d45b76127eb5a21d6495acd8d86bc4238daa36ee9ebc78877c8a21`  
		Last Modified: Fri, 17 Apr 2026 00:25:02 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
