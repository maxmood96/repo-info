## `amazoncorretto:8-alpine3.22-jre`

```console
$ docker pull amazoncorretto@sha256:0d423d5707bf4585ff83e251a7304e73b333a6329c7acd3315979ff563995e84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.22-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5b5758057618f1c54b240e4bb43b41a8a32a482eba06a6e97368173a0d81c35a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45552052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af480c6bfe47c43320fb8c3b5d53ad94ba17ea2e50d9ddfcc621b37551c202bb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:23 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:22:23 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:23 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22f33d2ff707b9769c0ecd693cbe244f3d816c736cbb3d7eed700fbf0e384f6`  
		Last Modified: Fri, 17 Apr 2026 00:22:34 GMT  
		Size: 41.7 MB (41743863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:cdc90dfebdd9b6ebb86d8492bbbd785df38d76720f9efa224bfba3c9c567d7c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.1 KB (197145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b76fd46f8b52f158e744428ab59ed134cfce1b99a275de12a520229d05cd6b53`

```dockerfile
```

-	Layers:
	-	`sha256:3ab270f0e752a96f7bcdc93de9b3f245cddddd6120024ba33dd0772802b05e11`  
		Last Modified: Fri, 17 Apr 2026 00:22:32 GMT  
		Size: 188.5 KB (188490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d77e421c610ac98b2885901f681c05a81a0054abe052d0dd64018b22487b956f`  
		Last Modified: Fri, 17 Apr 2026 00:22:32 GMT  
		Size: 8.7 KB (8655 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.22-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:789c708fdcc5cdc99779db99a44f20d668f6d49f3ab1b70563bfd417dfcb9bde
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45600075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ce05adf5ee6b99cab24608fb6424351afdcebfece6682b486384f9a0256f11b`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:20 GMT
ARG version=8.482.08.1
# Fri, 17 Apr 2026 00:24:20 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:24:20 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:24:20 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c5f3bf0c444aed7ce046162ba26eebb1d3eeb693680aed314b75c3ea9ff7fc7`  
		Last Modified: Fri, 17 Apr 2026 00:24:30 GMT  
		Size: 41.5 MB (41458181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b60ba0413a9bc527cc58546f40de421b82eb44e706bf4efdd3353e14e80fb11f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 KB (197333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b79e23583e4296fad99b55feb0bcfa293c06dee20c1f3a015bb1778c98eee8f`

```dockerfile
```

-	Layers:
	-	`sha256:060e8e1a8c434e46bd72d89e448463a130e985860c06153b957a06d9a919560a`  
		Last Modified: Fri, 17 Apr 2026 00:24:29 GMT  
		Size: 188.6 KB (188598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c1485deda4487ff3cff10134040a43f5870f7bd816340746f51a15e71404777`  
		Last Modified: Fri, 17 Apr 2026 00:24:29 GMT  
		Size: 8.7 KB (8735 bytes)  
		MIME: application/vnd.in-toto+json
