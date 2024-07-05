## `amazoncorretto:22-alpine3.17-full`

```console
$ docker pull amazoncorretto@sha256:9ec1912b4e19702231362791ad1c9e5ec3bd765859972863beade7d2a5a099b6
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:22-alpine3.17-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3990a589cfa7c1f7e8505e99f4bc8665cab6eec345472bc9bad21c24cd555a03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **161.5 MB (161474320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac7642bc0d5f65c7aaea44abab804841cdd75bb62d0436ffe2597615ac22982`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:cbcddefa487fb5085857fbba16854e06e53f93295bbf36ef1968a0b89835cad7 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=22.0.1.8.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=22.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:d4d4d3fb47b069ab78ba1600d105fadeed3980dd3c7890c36f31e9148c2b60d4`  
		Last Modified: Fri, 05 Jul 2024 19:56:33 GMT  
		Size: 158.1 MB (158084357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:17f79f3be4145c3440fcd2ca56f64fa1f19c65c438ae854b821fef9fb6ddd740
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.8 KB (385789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131501401a86ed464079ec4b6f8e719bda83b12e4fce8b4975efe946de0a9ae6`

```dockerfile
```

-	Layers:
	-	`sha256:dd32b743c72c8ed94fdcf3beb84dd27749be06b662165297a5225d623429a5ab`  
		Last Modified: Fri, 05 Jul 2024 19:56:29 GMT  
		Size: 376.6 KB (376621 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:56ca3adeb13382dbbb0d79fde17a4028c5da24f55d215a1017e34a33db2003a4`  
		Last Modified: Fri, 05 Jul 2024 19:56:29 GMT  
		Size: 9.2 KB (9168 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:22-alpine3.17-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:47be542d25001249010a373f8913a59aec66b3882f0595466d1a5324c18aebd1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **158.7 MB (158707319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f44374019cae326441668156a3c600ed1395a03c4461e63dec8fc6f0db9812`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Apr 2024 21:21:40 GMT
ADD file:deb5b1c3cd4e7a5be179620c767b9d7bfac29f2544596a65b760460e7a645c51 in / 
# Tue, 16 Apr 2024 21:21:40 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 21:21:40 GMT
ARG version=22.0.1.8.1
# Tue, 16 Apr 2024 21:21:40 GMT
# ARGS: version=22.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-22=$version-r0 &&     rm -rf /usr/lib/jvm/java-22-amazon-corretto/lib/src.zip # buildkit
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
	-	`sha256:345fad23a7524604e4cd5b9c57304d918aac2b29c199bfe0cf4894c134cda872`  
		Last Modified: Fri, 05 Jul 2024 20:31:08 GMT  
		Size: 155.4 MB (155434733 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:22-alpine3.17-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:8096c2654485fe812b59c823e280eede39f0daf33e1f11ce0d46a2718660bf72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 KB (384867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68e449934a8f66202952bb741dc788e1cc5cd7d1d2c4bd3f053d25fb20fe4a25`

```dockerfile
```

-	Layers:
	-	`sha256:3903618bd5ca13375276f07e1907090a9021a345635e0c0522cd148e94baf7ef`  
		Last Modified: Fri, 05 Jul 2024 20:31:04 GMT  
		Size: 375.4 KB (375398 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8a54797c3dd821e7e35391e128de89a5e2bd154dcb402f3f18e6b637eea6c57`  
		Last Modified: Fri, 05 Jul 2024 20:31:04 GMT  
		Size: 9.5 KB (9469 bytes)  
		MIME: application/vnd.in-toto+json
