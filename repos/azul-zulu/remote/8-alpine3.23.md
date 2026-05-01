## `azul-zulu:8-alpine3.23`

```console
$ docker pull azul-zulu@sha256:e028a2353cf34430b03d8d52a5ce1f7e79902f3ea7068b95a58bc3416fc7b133
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `azul-zulu:8-alpine3.23` - linux; amd64

```console
$ docker pull azul-zulu@sha256:83352f345a026d1eb57d02df9243e95f3c54c63021f6b7102ad2a659b1f6641b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60338612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39d6fac2e668a1f4eb46d3666ce1fca316c854b9062dae41afb9732d0da702c9`
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
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu8-jdk=8.0.492-r3;      java -version # buildkit
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
	-	`sha256:0efd8085e86fa9a4d4386b56315213b22d3cce4b3323a4639edbd86844eb7470`  
		Last Modified: Fri, 01 May 2026 00:22:13 GMT  
		Size: 56.5 MB (56474423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:31958bf88a7e9a11820690bc78ef6a5369d520219af2bb0c10224aa9d8e8921c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 KB (7790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9c219a7040ade82af24b56ecab19f2ce01682f96ddf5cbeff1d71296ca1b0de`

```dockerfile
```

-	Layers:
	-	`sha256:9989d4e769752fe18341fa760f7da9b859a590d044904f5c7e5f7d4aa042989f`  
		Last Modified: Fri, 01 May 2026 00:22:11 GMT  
		Size: 7.8 KB (7790 bytes)  
		MIME: application/vnd.in-toto+json

### `azul-zulu:8-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull azul-zulu@sha256:2894d89d0f6662a014666d65fbe6da209ee0079d076ff8bc7b7964dc8ac6ea35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59870067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7402741f0191b6469091e994036405bb750984241e3e808de05010f9a8e4eb3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 01 May 2026 00:19:33 GMT
ARG REPO_HOST=repos.azul.com
# Fri, 01 May 2026 00:19:33 GMT
ENV LANG=C.UTF-8
# Fri, 01 May 2026 00:19:33 GMT
# ARGS: REPO_HOST=repos.azul.com
RUN set -eux;      wget -O /tmp/azul-signing.pub https://cdn.azul.com/public_keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "6c6393d4755818a15cf055a5216cffa599f038cd508433faed2226925956509a  /tmp/azul-signing.pub" | sha256sum -c -;      mv /tmp/azul-signing.pub /etc/apk/keys/alpine-signing@azul.com-5d5dc44c.rsa.pub;      echo "https://$REPO_HOST/zulu/alpine" | tee -a /etc/apk/repositories;      apk add --no-cache zulu8-jdk=8.0.492-r3;      java -version # buildkit
# Fri, 01 May 2026 00:19:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/zulu8
# Fri, 01 May 2026 00:19:33 GMT
ENV PATH=/usr/lib/jvm/zulu8/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5315eb5f5bb36cbf30bcdd039f57e46916be3bfef1528972d258754df968c4e`  
		Last Modified: Fri, 01 May 2026 00:19:43 GMT  
		Size: 55.7 MB (55670197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `azul-zulu:8-alpine3.23` - unknown; unknown

```console
$ docker pull azul-zulu@sha256:0571715fa7b8b7452c91b9297db9793af3e048fa105bc333680ee899e8243d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f80023132a13caabd5a9debec9f5644d85594a875179eae3cf4387af187782f`

```dockerfile
```

-	Layers:
	-	`sha256:70e842728c5aed8e89c731f4bc48bcaa5f57f1ca84e03e12525c2c907defa09d`  
		Last Modified: Fri, 01 May 2026 00:19:41 GMT  
		Size: 7.9 KB (7894 bytes)  
		MIME: application/vnd.in-toto+json
