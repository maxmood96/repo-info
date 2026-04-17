## `amazoncorretto:17-alpine3.20-jdk`

```console
$ docker pull amazoncorretto@sha256:7716db185c5fd3a061b425781e97a85c76398d207ff21fdd60bc05d84b0c3968
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.20-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:b28fb5f78c4f95ec706d41bfd1c185ab4734a7dfd77389994f6cd14901ad7271
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.0 MB (151986600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06fa12efa840cebd7cb2c8ffc1d2ec48e4921248adf5a16393f0a6d347db6901`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:26 GMT
ADD alpine-minirootfs-3.20.10-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:26 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:22:33 GMT
ARG version=17.0.18.9.1
# Fri, 17 Apr 2026 00:22:33 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:22:33 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:22:33 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:22:33 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:25f1d6b1951ac8eb3740558fe94cb83d377bdadf95fd9f98b50d2e1b96130471`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.6 MB (3630321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:555f064e1766470c84bda64e1810b04cfbde2c35ad2deaf9c803bb81836d28c0`  
		Last Modified: Fri, 17 Apr 2026 00:22:50 GMT  
		Size: 148.4 MB (148356279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:b03f181e6acc26d4c51362eb6b566539fd3a22641872f576b4f837df811cb7e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **590.0 KB (590028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12127540e5e35a5f2919fdd381c6c2d9e0e989b8862719e1316fa5c32f3ac8f4`

```dockerfile
```

-	Layers:
	-	`sha256:fd4cfd7b0190276a96e8762f1f7bb53830e7750ac24b0ba1fd695f4ea1ab2d6a`  
		Last Modified: Fri, 17 Apr 2026 00:22:45 GMT  
		Size: 580.7 KB (580654 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d79154e63857338998bde93af685215047b9b1528be1f12e645064e175df5c8d`  
		Last Modified: Fri, 17 Apr 2026 00:22:45 GMT  
		Size: 9.4 KB (9374 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.20-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:1877fc68833aa0355eb5ac7fac0b316465ccb9164d898bf30224afe0e06b44f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **150.8 MB (150810854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6aad1b2a74bf2cd011a0a982020999e2d58d81b775a015774244baaa1a5ce04`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:24 GMT
ADD alpine-minirootfs-3.20.10-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:24 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:24:40 GMT
ARG version=17.0.18.9.1
# Fri, 17 Apr 2026 00:24:40 GMT
# ARGS: version=17.0.18.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Fri, 17 Apr 2026 00:24:40 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:24:40 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Fri, 17 Apr 2026 00:24:40 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:3f26bc2dec0b515f1c2818f6e13a8f1da1f88179a008445d4e587233386bff78`  
		Last Modified: Thu, 16 Apr 2026 23:53:29 GMT  
		Size: 4.1 MB (4092319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91f1fc3a01979fc2d471fec4d1d9e18deb0ce328c1aac176ef6b8adf1d5f362f`  
		Last Modified: Fri, 17 Apr 2026 00:24:58 GMT  
		Size: 146.7 MB (146718535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.20-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:46ed7f420eee013249cbac13b758603aff3350c281cba6c35d8683d1b2167488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **589.6 KB (589551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8cebfccda40f1bd5b9041306b21647485626c669e97751a841079cb91615265c`

```dockerfile
```

-	Layers:
	-	`sha256:4a00ee79caddec4c4a7eca1e0c69043830c388d23d09c32e97da2362c4cd85e6`  
		Last Modified: Fri, 17 Apr 2026 00:24:55 GMT  
		Size: 580.1 KB (580073 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f059d02587ff2ffe92f3e5ce2b42e69d8992380e970ad3ee0016802885e70ab`  
		Last Modified: Fri, 17 Apr 2026 00:24:55 GMT  
		Size: 9.5 KB (9478 bytes)  
		MIME: application/vnd.in-toto+json
