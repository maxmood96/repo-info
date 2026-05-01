## `azul-zulu:26-headless-alpine`

```console
$ docker pull azul-zulu@sha256:92decddd1283b710902a9d541987410e250c4b359e469cd1291c2229d2d4c1da
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:26-headless-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:7d06e952a263ac763b4840411a617717bd201c13443f6ed1fae1648b8b13f9f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **184.9 MB (184917858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:163c488c77797601a2ebc4e97382711d25ca86c6b65b60e97fb496265cb90c9b`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:44 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:44 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:44 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu26-jdk-headless=26.0.1-r1;      java -version # buildkit
# Fri, 01 May 2026 00:22:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Fri, 01 May 2026 00:22:44 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:22:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d55871652edb792086cce0ff94d25a26b983b0a58035e5c8d3584efe34238e`  
		Last Modified: Fri, 01 May 2026 00:23:02 GMT  
		Size: 181.1 MB (181053669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f1114024da694f2fad828eb878e6bd0ac8088fc729a0fa79993854794391a513
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1e6a03a3f376118b249af82a98c3d4fd011f2f974458c19ec69c95357b69f0`

```dockerfile
```

-	Layers:
	-	`sha256:7a58249af10690eb038bbc0caa846cba7dd1eeaaee6e05de537c2bb350deb4d9`  
		Last Modified: Fri, 01 May 2026 00:22:58 GMT  
		Size: 7.6 KB (7578 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:26-headless-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:17d44ee3df2df62e4745aede9623d67582c153fce890a05b7a3582be65e25164
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **182.8 MB (182755488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8454603498e70078e3486ff78c8c52e956ea31b671d27b918543861a92c2eb16`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:20:33 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:20:33 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:20:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu26-jdk-headless=26.0.1-r1;      java -version # buildkit
# Fri, 01 May 2026 00:20:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu26
# Fri, 01 May 2026 00:20:33 GMT
ENV PATH=/usr/lib/jvm/zulu26/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:20:33 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ffd01dca1276bb0e8c2108dd2ea5710c575224bf5472d2de76c773385dc1e4f`  
		Last Modified: Fri, 01 May 2026 00:20:51 GMT  
		Size: 178.6 MB (178555618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:26-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:70ec79c2b14ca7e160141dc9eb6ae2ca67cbdc41d1a96c8b4d94010f2223ba49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:693842217ee3eb5c545ebbaa605b2350d4a752ad0db7469fbae1fc1926158502`

```dockerfile
```

-	Layers:
	-	`sha256:f3625198363043792dcba34cebd2087f0e1b68ec085998ea5ecfbdd429b379cb`  
		Last Modified: Fri, 01 May 2026 00:20:47 GMT  
		Size: 7.7 KB (7670 bytes)  
		MIME: application/vnd.in-toto+json
