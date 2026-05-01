## `azul-zulu:8-headless-alpine`

```console
$ docker pull azul-zulu@sha256:820155f116832e02a005794c3c61b0709413c55f10320ff57722b028beb9c785
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-headless-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:1b9fc34f8fbb004cf22f1f27eae97c0084f4db8ced224fb499c3a2762334639a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57541556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df462b76a959ad6bb9af69baca235862d80897da43ff99da3b64eae6f6df9f56`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:03 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:03 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:03 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu8-jdk-headless=8.0.492-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:03 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Fri, 01 May 2026 00:22:03 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e80db1cc2f3ff35cfb4a1a6675f05cce2aa8a8923925b6978fec9186aeb2e26`  
		Last Modified: Fri, 01 May 2026 00:22:12 GMT  
		Size: 53.7 MB (53677367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:4210891e5fd6ce25fe3dc7ce43942bdb3102358ef697a72f3d8b0ac8549eda64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba9bf489ae7162513178e0861f8b28ddf7e50f85c74f26ea54c5e33470ece444`

```dockerfile
```

-	Layers:
	-	`sha256:e7839c0c06f765210be82d025d5cb23ea549e6359f69a84e4d44c5103b91d689`  
		Last Modified: Fri, 01 May 2026 00:22:10 GMT  
		Size: 7.5 KB (7550 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-headless-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:be1ad4b4e62ce96db81d137b2861f671862044a8fd455d9c54eda8d006d029aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (57036477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bd2ce4c9efd4f9d27f2f9b6eb032aaa27006cb1d7ec54242a64b4f0abf250bc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:19:39 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:19:39 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:19:39 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu8-jdk-headless=8.0.492-r3;      java -version # buildkit
# Fri, 01 May 2026 00:19:39 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Fri, 01 May 2026 00:19:39 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29848eaea396efe39a281b2e87ecb6f8e48ec34b3b1a7ee5cbcb654b9e436ad`  
		Last Modified: Fri, 01 May 2026 00:19:49 GMT  
		Size: 52.8 MB (52836607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:281e131945a13077f5dada25adbf00382294f2881456fc66a7a3c4c7ebed8542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fbb56d6e501f59f5a72ba470c82158c8fef806052e0098592982811b3a068aa`

```dockerfile
```

-	Layers:
	-	`sha256:eefcef0ceb9f2e59792e8c999d4e2d2584f0906d706aa3278dd8a6fc62888143`  
		Last Modified: Fri, 01 May 2026 00:19:46 GMT  
		Size: 7.6 KB (7643 bytes)  
		MIME: application/vnd.in-toto+json
