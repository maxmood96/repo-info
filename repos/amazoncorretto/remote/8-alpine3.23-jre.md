## `amazoncorretto:8-alpine3.23-jre`

```console
$ docker pull amazoncorretto@sha256:036a13f3c57470ec2356bfbd9fc81b3d9b16466143b4ea7d4e11548deebd4150
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.23-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2f64ed486e75dfb7de9c9641f35b105668d3532b7010563fc063b13e8f2e363f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45607153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61523bdafa1e72ac111969cbf14f47f23bc2a312deb0907c8e8f30a5723586f0`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:24:17 GMT
ARG version=8.482.08.1
# Wed, 15 Apr 2026 20:24:17 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:24:17 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:24:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b759f6e6c922f469e628a420a0ecbde7af4069e2c9294fe369078f8127833b`  
		Last Modified: Wed, 15 Apr 2026 20:24:27 GMT  
		Size: 41.7 MB (41742964 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.23-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:c0106e2af9d8efbc51ab6bf8d2e6f49573ec10d73dcaaf210b1db73c7efde9f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.2 KB (197187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e51ef3526a16454b26d2802236c9c30edc4a1adf007c581f1faed9e111b71132`

```dockerfile
```

-	Layers:
	-	`sha256:2d5cbba671ee937c1df08d8ea04b652bff843ae9b9466eb9b9a2e641d1e7c7d9`  
		Last Modified: Wed, 15 Apr 2026 20:24:26 GMT  
		Size: 187.9 KB (187871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b7360d9e6af3e0aa882ff2164e31b0b5c8472bbc4eaec096cd1080e52024c68`  
		Last Modified: Wed, 15 Apr 2026 20:24:26 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.23-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:4882274ab7ac6933af5f57f7683cfdc3b1160461b026fdc60f8bb420ae2ef30a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45658873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54e44d2d56ffe5cf3f8f58278060b8f58e01a13e27b8559a78ec0d45e2d83d96`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:23:24 GMT
ARG version=8.482.08.1
# Wed, 15 Apr 2026 20:23:24 GMT
# ARGS: version=8.482.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 15 Apr 2026 20:23:24 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:23:24 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf334141f658b7eed6a549ce03689334a547200475dfbbc3bcde888041e4462`  
		Last Modified: Wed, 15 Apr 2026 20:23:34 GMT  
		Size: 41.5 MB (41459003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.23-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:721b7fc27103c2efaf1a57abfc953bbfbd328399c95b224bc0d0d575b294c18e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.8 KB (196773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f51f15cc909231aabf2bbed7d574efd28ee4643c8d0f39b43e9cae9f641f33d`

```dockerfile
```

-	Layers:
	-	`sha256:b98cb7011ba582b76c3c9aada8ed86e6eb2d9303589dfe64e1769d4d186b12db`  
		Last Modified: Wed, 15 Apr 2026 20:23:33 GMT  
		Size: 187.4 KB (187353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e7509e8fafa279eaefce72cf1403b6d06bf66e8e485523e406a92a049f6db19`  
		Last Modified: Wed, 15 Apr 2026 20:23:33 GMT  
		Size: 9.4 KB (9420 bytes)  
		MIME: application/vnd.in-toto+json
