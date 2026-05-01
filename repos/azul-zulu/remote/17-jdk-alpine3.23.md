## `azul-zulu:17-jdk-alpine3.23`

```console
$ docker pull azul-zulu@sha256:16f1798d8295dd334f775486a72ce3cef48004d7faf826a71e8d0e8797805573
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:17-jdk-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:5042a9923122777fa1c95f86f077a049eeb8100a65f5db0642a7ef9537328f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.2 MB (152246349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b8be3c938670c62f15d0c2f67f1ae49befb79d9c27a0050f09a4d0e05e6c7d2`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:18 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:18 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:18 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jdk=17.0.19-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu17
# Fri, 01 May 2026 00:22:18 GMT
ENV PATH=/usr/lib/jvm/zulu17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:22:18 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1e51fb061ea31a99e323b9506090c479749e9d7cab2029411448eccc571c74`  
		Last Modified: Fri, 01 May 2026 00:22:32 GMT  
		Size: 148.4 MB (148382160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:941f18168aa6431709d7cb43e84b02a070650c451eaa43526209e302f587b2b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faa14d01e9353b240e33c899fbede87c5d5dc29dff5639817e9663ce689807b5`

```dockerfile
```

-	Layers:
	-	`sha256:c2d6086501c2cf5260aef1fa3a4ad637099c7b04a8d9713cb6c456fc18b337b7`  
		Last Modified: Fri, 01 May 2026 00:22:29 GMT  
		Size: 7.8 KB (7822 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:17-jdk-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:b62a5fe31db29cf7c445bbd8f0c994ec4c64767bb0ee07a28855f5ebd8d08965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.0 MB (150019986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c32d6698685517aa5822f46ebccd867add9bcb325ea44a2ee448e9b646f40a`
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
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu17-jdk=17.0.19-r3;      java -version # buildkit
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
	-	`sha256:078c3d29924610850675382aeff279665ac88e3ce5d7f5cf787f0a033dc2e430`  
		Last Modified: Fri, 01 May 2026 00:20:21 GMT  
		Size: 145.8 MB (145820116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:17-jdk-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:a4fe3889273dbf897defd8f93e1756d6f50d20323c8fb2168731245b2659c00c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9128e17b54daaf1a281a8f33aa1a72ca10306b2bf090b0701b92c3ce4f5ead6d`

```dockerfile
```

-	Layers:
	-	`sha256:b9403adc3a07d54cbb23c672c54bba848cd6011071aa4bdcd3f3fc435fb81f03`  
		Last Modified: Fri, 01 May 2026 00:20:17 GMT  
		Size: 7.9 KB (7926 bytes)  
		MIME: application/vnd.in-toto+json
