## `amazoncorretto:26-alpine-full`

```console
$ docker pull amazoncorretto@sha256:5f73844deb7a511f1f3f257525968a5175cd669b9d1abb039db21682c97cff8d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:60ff91625eaa7d5be803d306441abd00bff3afa5d3b352018d9e003fbd34b04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188795862 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da37c421d84d4af34f9eb23ff99555c79bc24b8772cab5b7bb85fee3aedfee06`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:53 GMT
ARG version=26.0.1.8.1
# Wed, 22 Apr 2026 21:35:53 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:53 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88be8c3d90eed058e55f5a122634ea50925487762da352f53cda90264990f1e`  
		Last Modified: Wed, 22 Apr 2026 21:36:14 GMT  
		Size: 184.9 MB (184931673 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a75bbbd2b09b56ea8b82de1cfd47e1bd55194952d0ba51ee11fcf1fe38bb0fa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.3 KB (598296 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ae745cb3cf9662fc53b64201d5dc6f08161793431523f9701c26c243ef52255`

```dockerfile
```

-	Layers:
	-	`sha256:7d8469ea79dccb8ffc57b55ef066cc542724f7d8e7f03a4c6b3abbdc24a896b4`  
		Last Modified: Wed, 22 Apr 2026 21:36:09 GMT  
		Size: 587.6 KB (587619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b2e4757d044646db1d5bf0f3e65f66387e45c53aec35b7693391b644653c4f39`  
		Last Modified: Wed, 22 Apr 2026 21:36:09 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bb4a4b8c445d4d4ec7f79d07bcabacf7c8258f0fdfdabb717a3d312a3c6716ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186703582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2073b64bd7df37abd97730772551961285d2e40a530d9497fb67e254990c457`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:35:56 GMT
ARG version=26.0.1.8.1
# Wed, 22 Apr 2026 21:35:56 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:35:56 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:35:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:35:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fa67111aa7644e52a8acc7c14d1b259392d7f024717cd29589e0f2dc52d3cd4`  
		Last Modified: Wed, 22 Apr 2026 21:36:17 GMT  
		Size: 182.5 MB (182503712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:24bfddebc0cc693889ebb80192309042ced713534be1578e451f1d9042df2846
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 KB (597261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405997332c46b4652676c47d2039e42ae8e3e4ef15ebb3da161944b062692039`

```dockerfile
```

-	Layers:
	-	`sha256:e79e71f17b3136a629359107b4877df99f7711e4419f2efe25df64225e980c8b`  
		Last Modified: Wed, 22 Apr 2026 21:36:13 GMT  
		Size: 586.4 KB (586433 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8cd903561c82cd4bd8e6f9bc9669a294316e52a2337e7a484ca5afdfc415033`  
		Last Modified: Wed, 22 Apr 2026 21:36:13 GMT  
		Size: 10.8 KB (10828 bytes)  
		MIME: application/vnd.in-toto+json
