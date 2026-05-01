## `azul-zulu:21-headless-alpine`

```console
$ docker pull azul-zulu@sha256:d98b38b39c624154792c929dafdf80a1ac320797afe6520aed6d80a5feaab467
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:21-headless-alpine` - linux; amd64

```console
$ docker pull azul-zulu@sha256:d2e723232c433810e17a777a0f5dd749c4210358bdca7510ba4acd177ff91e3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.1 MB (162136559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfc7d4bbf0e6ff9811faa9878e3ac5b3cd161e0496f5bda7ce0297d64bd7dbf4`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:22:25 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:22:25 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:22:25 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jdk-headless=21.0.11-r3;      java -version # buildkit
# Fri, 01 May 2026 00:22:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Fri, 01 May 2026 00:22:25 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:22:25 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd3a6c4ebc685e87c3326bffb330d7e165d443b991778e67c3807f6625423d0`  
		Last Modified: Fri, 01 May 2026 00:22:43 GMT  
		Size: 158.3 MB (158272370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:2acb106fc584cba582e2f97d5084aef861f979ec33d8be0e6166b176ba241985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 KB (7581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39c816b26e3e1848d1469330b3bc1fbbf7c99dd79c6e6126987486c36c286186`

```dockerfile
```

-	Layers:
	-	`sha256:0fae3cbecc56ef976497f4e0533a6009be40ffe2c934975da1c0c63a2205b066`  
		Last Modified: Fri, 01 May 2026 00:22:39 GMT  
		Size: 7.6 KB (7581 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:21-headless-alpine` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:4f7254a627a0f9779d28c9d85b04eff5d26aa3b8b04c56541a48e295eca6b5b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **159.6 MB (159632756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2de538f48660784f0ce2b3ac5f3dc6f34cedcf21757f22d024172fa234e290cb`
-	Default Command: `["jshell"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:20:21 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:20:21 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:20:21 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu21-jdk-headless=21.0.11-r3;      java -version # buildkit
# Fri, 01 May 2026 00:20:21 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu21
# Fri, 01 May 2026 00:20:21 GMT
ENV PATH=/usr/lib/jvm/zulu21/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 May 2026 00:20:21 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a87ea599637257846397922b96f77e178f7d33ddeefcf536dd946c0f08c1f579`  
		Last Modified: Fri, 01 May 2026 00:20:37 GMT  
		Size: 155.4 MB (155432886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:21-headless-alpine` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:c7805f037054e6c05e98a19033a88af3e17b31073b15188d2f0d6cca8e56f800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 KB (7673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddd35f3d2551a93a9cc5a4f65dbacf20197cdc66cd184b5f0eb1dd751d613f56`

```dockerfile
```

-	Layers:
	-	`sha256:440f57e855e937ab0ae2ff3f1b8e8a6d93e2088decfb44035660f4d2864f8509`  
		Last Modified: Fri, 01 May 2026 00:20:33 GMT  
		Size: 7.7 KB (7673 bytes)  
		MIME: application/vnd.in-toto+json
