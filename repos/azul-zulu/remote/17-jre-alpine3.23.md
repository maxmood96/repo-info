## `azul-zulu:17-jre-alpine3.23`

```console
$ docker pull azul-zulu@sha256:6d917290d86e8ef57bc04bcc04584dd97f5dc4f119a3359c1dfd57499e2eadf3
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jre-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:4726a2b70f9638cfe9c099a7bb25df2114cd738dd80038a59027301110ade356
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70676964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245fa70d680a43ca138ccd322e16e88c6a0f6de8989b79f4702e91911ef4b00d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:19 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:19 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:19 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jre=17.0.19-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:19 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Fri, 01 May 2026 00:22:19 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e96e41594e6642e1aabd906078718e8589884f07cddc829844dd9b1940ee5711`  
		Last Modified: Fri, 01 May 2026 00:22:30 GMT  
		Size: 66.8 MB (66812775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:1bb224274376401422754b0c1ad8ba12b4f685729de22d558f7edc74df35408a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a251172be6593c9702703dd7a849134b5f8942392b57e798deef4f6c52892ce8`

```dockerfile
```

-	Layers:
	-	`sha256:7e6c892407eefc8aab989da197fe997c5d2fac8c703a5eb1c0d1c42ef90279e3`  
		Last Modified: Fri, 01 May 2026 00:22:28 GMT  
		Size: 7.5 KB (7483 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jre-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:1fe42d9a3ea9e5bbca75b0fcafb2fbe65280115b0dcbf65a33d02a342560054f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69910594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc37fe13639834e479048f417533065d5a6e6f49be82477bf452ff1f9e946382`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:20:08 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:20:08 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:20:08 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jre=17.0.19-r3;      java -version # buildkit
# Fri, 01 May 2026 00:20:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Fri, 01 May 2026 00:20:08 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f681403d800808d6727bbc7069765077d3c4ca1d791eebcd172b147185a0c52f`  
		Last Modified: Fri, 01 May 2026 00:20:21 GMT  
		Size: 65.7 MB (65710724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jre-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4e547b195094071164265cbd94d22c73855eda8219e77c704c641aa4223638cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e1816173873669be2013305def6abba9c68086b2d599ca23abdcf480a30b108`

```dockerfile
```

-	Layers:
	-	`sha256:f4b6d6eaabe2870a56a2ef15266744bf772c82d0c5520cd5e66ceae93657d7b6`  
		Last Modified: Fri, 01 May 2026 00:20:19 GMT  
		Size: 7.6 KB (7575 bytes)  
		MIME: application/vnd.in-toto+json
