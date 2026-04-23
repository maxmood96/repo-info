## `amazoncorretto:17-alpine3.23-jdk`

```console
$ docker pull amazoncorretto@sha256:ec98313130de5de7ad13177111da8cd61b8a772c93d6be4a452f84bc679716b7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:17-alpine3.23-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:dd385e11ac99ee4c57b4e6e1b90abecc418034e693628f6ca86c6457822d242f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **152.4 MB (152447643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2dd2d858fa603ffef5dcff9779b80de9d40570431e95608c051286dbddefe07`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:25 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:25 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:25 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70996f4731d80bb777dc007c01bbb313c2d7205086bed0275a9259be9c42ec88`  
		Last Modified: Wed, 22 Apr 2026 21:34:41 GMT  
		Size: 148.6 MB (148583454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:1085d37e17228857697dc336e81bd12bdbe3d86a79ed2a249ca68a5c36ca81b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **594.5 KB (594498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00db195860163a805f8a79cd4625f052a90320f1657c9dc287a8a74f2598d29`

```dockerfile
```

-	Layers:
	-	`sha256:653e7fc0e18eab4effd93b0b8feb158872aa612f1e11f96cf19fff73dad2fb0e`  
		Last Modified: Wed, 22 Apr 2026 21:34:38 GMT  
		Size: 583.8 KB (583811 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b65951747c3fa1c16c0511ab6956118b31c4c4307e5f99de0b52574a96d8f82`  
		Last Modified: Wed, 22 Apr 2026 21:34:38 GMT  
		Size: 10.7 KB (10687 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:17-alpine3.23-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:5c5f0884824a1f1bc350251df2ade3a80cce21715472cbd0ab2f8e29da529aea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **151.1 MB (151137513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0320577a99a6cc942d3178e94a22a1d05f59f59a64ee17263ebb6612e8ef7ed`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 22 Apr 2026 21:34:22 GMT
ARG version=17.0.19.10.1
# Wed, 22 Apr 2026 21:34:22 GMT
# ARGS: version=17.0.19.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0 &&     rm -rf /usr/lib/jvm/java-17-amazon-corretto/lib/src.zip # buildkit
# Wed, 22 Apr 2026 21:34:22 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 21:34:22 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 22 Apr 2026 21:34:22 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0529315e3631a56927dc9186f923e06f688e00895e152f54e0716f3971048783`  
		Last Modified: Wed, 22 Apr 2026 21:34:43 GMT  
		Size: 146.9 MB (146937643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:17-alpine3.23-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6be096bb83b275e392e4fc627d8c14374cb9b11b0612d5b530dbb6d8253182b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **593.5 KB (593467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3fd01942a255fe8138e0e56a6b09036ff99b04322311b55076ea4ff1b76575`

```dockerfile
```

-	Layers:
	-	`sha256:8630d79b94d1bd2a84dd197144c77060b8ed24abaad993d261d474df4378b048`  
		Last Modified: Wed, 22 Apr 2026 21:34:39 GMT  
		Size: 582.6 KB (582628 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fae59676bed51ec09bbf326e2ce75fe79e6996a6ef60f5d4bfe8f09e4c975f`  
		Last Modified: Wed, 22 Apr 2026 21:34:39 GMT  
		Size: 10.8 KB (10839 bytes)  
		MIME: application/vnd.in-toto+json
