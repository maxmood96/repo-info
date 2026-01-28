## `amazoncorretto:8u482-alpine3.23-jre`

```console
$ docker pull amazoncorretto@sha256:805b6188b67f05b4505ef7cd9755fdd80a1b296901fd3bbd4dff75057c0c6abf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u482-alpine3.23-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fc14b91e95c7ee5d7b4967ae0c7f4c30cfab9250178dc7db3769ae43b1e28c63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45604820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ba78e04d8b33b0992c2d46f5119b7cca8848854a357cd194d8ad9da9d28cde`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Wed, 28 Jan 2026 02:43:40 GMT
ARG version=8.482.08.1
# Wed, 28 Jan 2026 02:43:40 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 28 Jan 2026 02:43:40 GMT
ENV LANG=C.UTF-8
# Wed, 28 Jan 2026 02:43:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f56bce2f690a45bdb524a96143280e7358469f0c8bc258d741956d49843af3bc`  
		Last Modified: Wed, 28 Jan 2026 02:43:51 GMT  
		Size: 41.7 MB (41742999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.23-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f88f34ec8928951a5d557bf633406af4d08b25e3e255e991086a8f4f1a6229d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 KB (197159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16f9cdd3386e1e2e3061612aecc7c57ec86e7dcd5d72fa48fbac3dcdac7511f`

```dockerfile
```

-	Layers:
	-	`sha256:3b8b20b166c324213296285ebb2739cfe57a7ecc973bbf80156dc639822244c1`  
		Last Modified: Wed, 28 Jan 2026 02:43:49 GMT  
		Size: 187.8 KB (187843 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94493e0a3deb0765ee00df49b15517d1c43fd2f13b313d5554975a0133f70826`  
		Last Modified: Wed, 28 Jan 2026 02:43:49 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u482-alpine3.23-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:fab8239f942f396478316f7daed2bec49cf8fa877b62ad4e3c76f2eebef4436e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45654773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d76888311ff5ec7c790679319145285757abab2934c20238a987a1170bd2e267`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Wed, 21 Jan 2026 18:59:06 GMT
ARG version=8.482.08.1
# Wed, 21 Jan 2026 18:59:06 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 21 Jan 2026 18:59:06 GMT
ENV LANG=C.UTF-8
# Wed, 21 Jan 2026 18:59:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:35 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2765a988a269006907aa5589f9f85cc938a2fabd4558c0e5a9bb24d346b5b857`  
		Last Modified: Wed, 21 Jan 2026 18:59:16 GMT  
		Size: 41.5 MB (41459034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u482-alpine3.23-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:af9b097b98b2bbb0ba31d570cb79e28094d8430b136e9eb6d0a0b6dc4278e9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 KB (196745 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:456521176c2bfc1f4353b418c40ebabb2463ac2f2c02ed48c153500482d6b54c`

```dockerfile
```

-	Layers:
	-	`sha256:87844206305ad4772793f5ce292e60a240d2f8b71ae873928a67236a2a8d0482`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 187.3 KB (187325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b08769c811d58964b4f3b24ace21f35a60c1e313f7666fa06fa33200df96a467`  
		Last Modified: Wed, 21 Jan 2026 18:59:15 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.in-toto+json
