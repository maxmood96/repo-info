## `azul-zulu:21-alpine3.23`

```console
$ docker pull azul-zulu@sha256:767658201c68a3fa94df85da842b29efa5b8213b23a37d62d677a61d69fd40b4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:81d0395e7bf62ad371eb9467a26a7d7d4285ac8fbee17753d675feb5f9289e7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.3 MB (165250746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e6e101ffbf2e4feae7ecff902d3c31b52d3cf263a55e811bf93031e492a1ee0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:23 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:23 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:23 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jdk=21.0.11-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Fri, 01 May 2026 00:22:23 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:22:23 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce3792a1cab996673fa1ee5b5850befb45b61ca94858e725412e7fd043ab344`  
		Last Modified: Fri, 01 May 2026 00:22:39 GMT  
		Size: 161.4 MB (161386557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:f003699c5f9c9d388457e63a182c774027f0830ff404fedee900fc4d26a79a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8814c839da20076bc1442ca4fab1f85164845ead51d6ae8febc56c6dd796bf6`

```dockerfile
```

-	Layers:
	-	`sha256:dd4cdb970b515916b0adbcdbc2f4f97637c8d4b8e8984f4eab9d78595d291290`  
		Last Modified: Fri, 01 May 2026 00:22:35 GMT  
		Size: 7.8 KB (7821 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:f01e8b2cb2d388dd7e9523960f5676b33aa8e6aeffb059f80ae1478c92e9d226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.8 MB (162809438 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15350737ec09b1f31e111ff0f39516b7a89bfe38dffd52e3eaffb925c17cc6c0`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:20:15 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:20:15 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:20:15 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jdk=21.0.11-r3;      java -version # buildkit
# Fri, 01 May 2026 00:20:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Fri, 01 May 2026 00:20:15 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:20:15 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:228bffb49a8cd294e8353ddf7d71760748a30e819d2d2b1ab9cdc03089f9147b`  
		Last Modified: Fri, 01 May 2026 00:20:32 GMT  
		Size: 158.6 MB (158609568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:078dc23b5a165c3553dfdc06b7bd8fbf2cb96d33497d0e2809f46409079624c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b7ae34f29f5512b5869ab4cc10b0d1d716110c47b59f0cfcbf21be75241b3a1`

```dockerfile
```

-	Layers:
	-	`sha256:5fd08f5e6c6a21b89a19d6fac56015abdea4fcba3a93c688fd5118371f74d799`  
		Last Modified: Fri, 01 May 2026 00:20:29 GMT  
		Size: 7.9 KB (7926 bytes)  
		MIME: application/vnd.in-toto+json
