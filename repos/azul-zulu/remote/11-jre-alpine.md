## `azul-zulu:11-jre-alpine`

```console
$ docker pull azul-zulu@sha256:adf8986c29d079b95841a4dda998e687d61a94010a8bcdca97efcb46703e9872
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:11-jre-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:7db9deb6a20e65dc43a047d672b81190c374f3bcfc6460f24f074fa5edbb50e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66186289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e5abae9fbbe54237ddb7a55cbd8d4f045da2645d180a9c123400d070417f2c5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:14 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:14 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:14 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jre=11.0.31-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Fri, 01 May 2026 00:22:14 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c913fd814cb01f7493eb68ec533c8c370e7aaa169b142552721ff611e14ac7f`  
		Last Modified: Fri, 01 May 2026 00:22:25 GMT  
		Size: 62.3 MB (62322100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:bf1ee7bbeabda10d44b324a8a973116a4793b6aa7c29785ad23d89c4db193746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 KB (7482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11a8f98a0d8896434f0281c696fa23a42921874edb7ad43f89fa52d20637edee`

```dockerfile
```

-	Layers:
	-	`sha256:669d5fbc8e17ec831e66f6ba65f2cdcd2064625fa1f2b43418840822df0f09c4`  
		Last Modified: Fri, 01 May 2026 00:22:23 GMT  
		Size: 7.5 KB (7482 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:11-jre-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f986b6eb33199a8919994883d47b76f9f94a118a9472d3c1de7e17a97e862889
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65322157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c843dfb9ec7222e27a667559c7d7785b6d312c73e1f388076e900da32faeaa71`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:19:59 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:19:59 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:19:59 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu11-jre=11.0.31-r3;      java -version # buildkit
# Fri, 01 May 2026 00:19:59 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu11
# Fri, 01 May 2026 00:19:59 GMT
ENV PATH=/usr/lib/jvm/zulu11/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dd2bc5f3cdf36b2fcd2139097a9de03a4f8f40e9f19b75168c241953b44ffc2`  
		Last Modified: Fri, 01 May 2026 00:20:11 GMT  
		Size: 61.1 MB (61122287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:11-jre-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:5f88249684fe856315a8f47a646c7c9edbf85a7f42e8fd58d80ea03834b7ab61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fbe6ad4674bb2ce350708e30f63bca2c9ea4d4b74b4be9b9e6a7a8c882191f7`

```dockerfile
```

-	Layers:
	-	`sha256:a009f33323b81a650be00a2fe0ef24c803c9b89ae5246e351a105a85ac806b91`  
		Last Modified: Fri, 01 May 2026 00:20:09 GMT  
		Size: 7.6 KB (7575 bytes)  
		MIME: application/vnd.in-toto+json
