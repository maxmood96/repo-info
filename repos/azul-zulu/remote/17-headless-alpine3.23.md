## `azul-zulu:17-headless-alpine3.23`

```console
$ docker pull azul-zulu@sha256:901d3d32f234eeba21bd36cd5023fea29c02c630920a6b3da8f1364bccf04896
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-headless-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:cc4ea7c194e18a3a661ca9d7618c69e4887cd6da6c724e151e504f4b9a3c8206
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **149.1 MB (149101768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a44549f11dbc5902c26aeb694f810a25b156e862f2d3560a9e56c35a7fe1e055`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:20 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:20 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:20 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jdk-headless=17.0.19-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Fri, 01 May 2026 00:22:20 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:22:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80aeda603293592298083cfc1f30f8deb0feb07aeb3365801c79a17ba980445f`  
		Last Modified: Fri, 01 May 2026 00:22:34 GMT  
		Size: 145.2 MB (145237579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:914853b1338e14d89390bd9221eacaa159335820f9ab4f9dcbd00f4209c9a9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1784b8be60ddb8acbeb5e98234ef4df5405e2910477c64140ab42d1d5a39b5a0`

```dockerfile
```

-	Layers:
	-	`sha256:e8789c0c21435c0173bb6e6fe7df8c6bf0fc4bc843ac9e8cf8030d30f57b4afa`  
		Last Modified: Fri, 01 May 2026 00:22:31 GMT  
		Size: 7.6 KB (7581 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-headless-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:013c8e215096aa2dc5514014ca3ac776243c4bfdc0a1168f4f3f78bc293fda9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.8 MB (146818812 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d11560ca309ed0947f457baeae8c8f3fa6fa508579832335e7cfcd599c9bcc0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:20:05 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:20:05 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:20:05 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jdk-headless=17.0.19-r3;      java -version # buildkit
# Fri, 01 May 2026 00:20:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Fri, 01 May 2026 00:20:05 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:20:05 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32eec197e20a6f69e7e3f6e0f575a7b68247ee2fe5c267ec915be54072b728dc`  
		Last Modified: Fri, 01 May 2026 00:20:21 GMT  
		Size: 142.6 MB (142618942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-headless-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:319374bd7d94481cba8add3ed4df2f2bc33f698bfad40478ff2a5184febb99cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbd5126a02dec0676b23a3ce47ded1c3abd36944bf30469ea41a11dd47c6d307`

```dockerfile
```

-	Layers:
	-	`sha256:eea14a9920eccd504141dd6cff37c83a7c7926e44d69b3dafef5d3c72f3dfccd`  
		Last Modified: Fri, 01 May 2026 00:20:17 GMT  
		Size: 7.7 KB (7673 bytes)  
		MIME: application/vnd.in-toto+json
