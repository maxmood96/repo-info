## `amazoncorretto:21-alpine3.22`

```console
$ docker pull amazoncorretto@sha256:b55053be9ea859889530f3b51ebaafb7c579c4d62ee3d3bb77bc535075f84067
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.22` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bf13a343c0c53338cdb307d9ccd5a78b4e6f2ad8bc1426e508a5d0f6224c1dd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.4 MB (165401275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2370bd4ecf61c557f2ebb4efa5a301a18dc89b250f64a9f407dfba5abe8381`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:56 GMT
ARG version=21.0.10.7.1
# Fri, 17 Apr 2026 00:22:56 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:56 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:22:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e7cfbade5da00bab0439f40fd9de6788f4275ae4410ba03c8d538217cafaea3`  
		Last Modified: Fri, 17 Apr 2026 00:23:16 GMT  
		Size: 161.6 MB (161593086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d2ad41b5e140f57488a6664cb7dc2dedf2937a274bf6c46834c1a804a9d8e95a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **592.4 KB (592413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c2483de0eec3507c54ae3aeae362bf9c78289ebae41398941ec7385d2bea27`

```dockerfile
```

-	Layers:
	-	`sha256:2f766e9a6c035f5a4ae416a576f5729946ce747cd50440a20b962c6e9db7aa1d`  
		Last Modified: Fri, 17 Apr 2026 00:23:12 GMT  
		Size: 583.0 KB (583039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2e45b2e4d618ae051ab53384d95bdf28b4bf2316e7239271d444bd5c09068f9`  
		Last Modified: Fri, 17 Apr 2026 00:23:11 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:a9f8f5cdb09ec0e627537a0544b6d2a9e37e32d60d1aa37eccd3548565bc3dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.8 MB (163756977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2eae524b2f96562d058b0054e6874dc6b890a03981cc97475d9cdbf98391c62c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:25:07 GMT
ARG version=21.0.10.7.1
# Fri, 17 Apr 2026 00:25:07 GMT
# ARGS: version=21.0.10.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:25:07 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:25:07 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:25:07 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10180e2dd62dc8e732b9f5beb4ea003ab8c4c55f37cc79a720f35cee31c2c00b`  
		Last Modified: Fri, 17 Apr 2026 00:25:27 GMT  
		Size: 159.6 MB (159615083 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.22` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b1917c100a8e0480915cc89ccf6a8b45e5c22d672a22f91bc65ecabfb9e2cc1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **591.9 KB (591936 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01274110c8c9131f1baa78160f020f8dbe5bfe718486b7a4bc255f3c39e86836`

```dockerfile
```

-	Layers:
	-	`sha256:71a9a4488aa8824fc59ad765695c49376c31d42f7aa1f604725c1c4d175fda6f`  
		Last Modified: Fri, 17 Apr 2026 00:25:22 GMT  
		Size: 582.5 KB (582458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:350505bfcbdaed8fb0286101c2ae35c8ea0f3d13493639acb1fce77cccd0fece`  
		Last Modified: Fri, 17 Apr 2026 00:25:23 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
