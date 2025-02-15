## `amazoncorretto:21-alpine3.18-jdk`

```console
$ docker pull amazoncorretto@sha256:4a81ed9d60305c7fc6819ea558331162dbddafc5aed115d5cb7bfa98189fb5dc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:21-alpine3.18-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:29263a8c3b3f6b7c31bfeb1642d2266bd23f30a4e25bd3747fe148a5ba803a57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **162.4 MB (162373704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f505819796c41c45baa73a53ec1550684525c72ef67c05181bab5afc8dbdb5`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.18.12-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=21.0.6.7.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 24 Jan 2025 20:03:54 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:44cf07d57ee4424189f012074a59110ee2065adfdde9c7d9826bebdffce0a885`  
		Last Modified: Fri, 14 Feb 2025 14:36:09 GMT  
		Size: 3.4 MB (3418409 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7793d961ab18f6c31d4f9e6b51af809c83b4158296608bfb983af58c71bb480f`  
		Last Modified: Fri, 14 Feb 2025 23:36:36 GMT  
		Size: 159.0 MB (158955295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:5b713eb710dd13acab0dd3fd129ce42b042e1daa7dfafc38a99f59b5414b6384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.5 KB (389544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e32a0ffb49bb80837fa584030abc9be4509d3ac5e805f38143f62a43190ae985`

```dockerfile
```

-	Layers:
	-	`sha256:aca3a849c026a47728a9a1703f34f931828a544f816c12eddee211fa5e648df0`  
		Last Modified: Fri, 14 Feb 2025 22:48:39 GMT  
		Size: 380.1 KB (380131 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ece7656e423114e4b681148c26a4fc02082003fa314718f15885ffce7fcced9`  
		Last Modified: Fri, 14 Feb 2025 22:48:39 GMT  
		Size: 9.4 KB (9413 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:21-alpine3.18-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:bfd01184f1d495f1b6666e6fb739ba09a57a822737cd22f0c6e672b8e5427b07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.3 MB (160277144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24f26f2554ea5b2b49c606dd2996843d2e1151d7ffa4e5548872ed7102012c17`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:05:14 GMT
ADD alpine-minirootfs-3.18.11-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:05:14 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=21.0.6.7.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=21.0.6.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-21=$version-r0 &&     rm -rf /usr/lib/jvm/java-21-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 23 Jan 2025 01:09:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f6b431426dd566e612639f03cd46e521b3133a043bb6b60edeeeef80d513e870`  
		Last Modified: Tue, 14 Jan 2025 20:34:06 GMT  
		Size: 3.3 MB (3341861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16149fb98927747995aacea4de7cc623298ba445fe9c41ca25d72eaff889d58e`  
		Last Modified: Wed, 05 Feb 2025 19:41:25 GMT  
		Size: 156.9 MB (156935283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:21-alpine3.18-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e0b2403cb739c8426b88d88e764e16634722f6d53d70887283f5e3c18e159de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **389.1 KB (389067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8189d369244ba9427d28270ee993e4cca2e330d7041809427dd4e637b78a2fb2`

```dockerfile
```

-	Layers:
	-	`sha256:8d333ca0a91ab8635e5adae36be46448e983bfeced40219e7dcde0ae7fdaf933`  
		Last Modified: Wed, 12 Feb 2025 08:10:57 GMT  
		Size: 379.6 KB (379550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76d190fe28bda82e2ce45df3b7dbe2fdce2e111b1bf9f7e5cc06e125e251740`  
		Last Modified: Fri, 14 Feb 2025 22:48:40 GMT  
		Size: 9.5 KB (9517 bytes)  
		MIME: application/vnd.in-toto+json
