## `amazoncorretto:8-alpine3.17-full`

```console
$ docker pull amazoncorretto@sha256:e42f18a9016f4e3e3ea2db4787dcf7f22961491e4189ffd3e0a8082dca43023c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.17-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:ec33878fc43a2729dbf6616d9abc94931998028c7eedb291862c5173082182bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.6 MB (103560778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9a2fd97571aa4a22eb1e7b8b6c004f3eb46948dc3a7af200147d4b157bdae2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f9202480295a4ef9cc62343dea568a5840b58bc68a1970045d30f3077a46a471`  
		Last Modified: Thu, 20 Jun 2024 20:18:01 GMT  
		Size: 3.4 MB (3389963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f0d0814f3d0a0884c21a3c9076fb9f1ec9f2f19066a1972b3b6339267675d3`  
		Last Modified: Fri, 05 Jul 2024 19:56:03 GMT  
		Size: 100.2 MB (100170815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:49981f1691d5b27c20a34edc4949b3bbf3aeca49b86a4bd0aa960e8791385c17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.2 KB (247249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f88b4d250a21480e581972129ef8856c38c96133c55513eab174dda5c8e9b3c`

```dockerfile
```

-	Layers:
	-	`sha256:7fadef77004dec36748ab9732a7a2d73ecec749998cbeb3982d2169d568f00b8`  
		Last Modified: Fri, 05 Jul 2024 19:56:02 GMT  
		Size: 238.1 KB (238096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f0d4edfa1749f3cf326d51b32f409a3e40b5d6e9c686f689adb896f8e3b6424`  
		Last Modified: Fri, 05 Jul 2024 19:56:02 GMT  
		Size: 9.2 KB (9153 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.17-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:583dc1331acbcabd16517535f58852e831dfa54607450196b76987d0f63752ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **103.1 MB (103091756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb02c27a3a8468abda13cc9c8827b65d5af10362102800040a37e83ad9416a32`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=8.412.08.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=8.412.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Apr 2024 21:21:40 GMT
ENV LANG=C.UTF-8
# Tue, 16 Apr 2024 21:21:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Tue, 16 Apr 2024 21:21:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:e45a60384f0269bd8514e16cf71591639353996e62a144763c5e519b386ac31c`  
		Last Modified: Thu, 20 Jun 2024 17:41:39 GMT  
		Size: 3.3 MB (3272586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e44a88d4aeecacb9e4c9a001ac0889a50772cbdbc6a44be24991b317a24d5d8c`  
		Last Modified: Fri, 05 Jul 2024 20:00:15 GMT  
		Size: 99.8 MB (99819170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e8f6b4c810069680644e2ec588fee4bbe2dcf07e23c18ff354b60ab0eb33313d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **247.7 KB (247680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5d8500415f393adb766a8061465fd38b1bb6fbaa25910fce5e245d911e8e9c4`

```dockerfile
```

-	Layers:
	-	`sha256:a43dc675c11840932e8cc21241ca744f989efc245b4642e0108c8c4204c985a4`  
		Last Modified: Fri, 05 Jul 2024 20:00:12 GMT  
		Size: 238.2 KB (238228 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a881acc2a0ab7487a7dcf6c0f0a27174cd9e9b8d271978b2b2736844822123c9`  
		Last Modified: Fri, 05 Jul 2024 20:00:12 GMT  
		Size: 9.5 KB (9452 bytes)  
		MIME: application/vnd.in-toto+json
