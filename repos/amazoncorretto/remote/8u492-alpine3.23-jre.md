## `amazoncorretto:8u492-alpine3.23-jre`

```console
$ docker pull amazoncorretto@sha256:16bb0bf9b42f1bb5077a27a2514565c88fcd4cd1de6dc848acc0a02a062c4ce0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u492-alpine3.23-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9662a3482ff6705ad28d89006dd5f781759780c17d6fa13c6d5f5653aab073bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45614249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f293c729c0c5db1b14346c6f89c826df78e11c68cce23a3f1a94f46495cdd4ca`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:59:04 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:59:04 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:59:04 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:59:04 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d98ae2d7ad953a7dfb76cdea85d47b230d758759303255f4982818c8917462d0`  
		Last Modified: Fri, 08 May 2026 22:59:13 GMT  
		Size: 41.8 MB (41750060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.23-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:82f6120cfdf4e610f047c9c33c6372f4fec8555daf5bca976bbdac1d0468a6bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 KB (197187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9496ca467b5985a319d2e294fb067683b5563bfd39905e608a5021b35532a9ad`

```dockerfile
```

-	Layers:
	-	`sha256:ac6f94da983d3dcb6cd9952703a26db0267d0111c7a9ae9f378e2029013e7849`  
		Last Modified: Fri, 08 May 2026 22:59:12 GMT  
		Size: 187.9 KB (187871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f6ce54afcaf86922e9f081d0919e3dd47ed95c5559992c4b466b135f316252e1`  
		Last Modified: Fri, 08 May 2026 22:59:12 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u492-alpine3.23-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:0137c960539d3f85c6de2b8f123cc1bd249b20d08d24874403823e714232d762
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45667628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c97b73f703f07519b002f26b7f2a0292e938ce6768e78dce5308862b8b639eeb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 08 May 2026 22:48:38 GMT
ARG version=8.492.09.2
# Fri, 08 May 2026 22:48:38 GMT
# ARGS: version=8.492.09.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 08 May 2026 22:48:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 May 2026 22:48:38 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ae09c3bddef3f28271c0c42f64e08484135efc4df4f19d5a35f8bb4028500b`  
		Last Modified: Fri, 08 May 2026 22:48:48 GMT  
		Size: 41.5 MB (41467758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u492-alpine3.23-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:ffe22251f2bf6a8eee066a36d28ead5821acf2978c2708dd539b00c1d1ff368a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 KB (196773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8ec006dd12eeac15e5e33edffac5512abd664fcbb34e869f4d77e3081cba3c4`

```dockerfile
```

-	Layers:
	-	`sha256:b29bd1473ca35b09dad3c93eadbdd1c85905fdab9ef5756a63b87e4f8ea5f572`  
		Last Modified: Fri, 08 May 2026 22:48:47 GMT  
		Size: 187.4 KB (187353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc0f9cb69513496913f208277e0d80aac62397f8997f80811acb564082fa48c4`  
		Last Modified: Fri, 08 May 2026 22:48:47 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.in-toto+json
