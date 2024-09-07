## `amazoncorretto:8-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:cb20cf9e1588ba56732dda28a214ef6e2fef719292343a2669eb78da83f635b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.18-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:66a96696c58ca624830b9a5c6a4e97223cf99efd6b7aaa44b2f906c2f0f16b91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45015811 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f3b52419e3bfa663718bb8d2d9792d870baea360674fd5376205e66dc3dbcc`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:5dd525c57625a3a84d57d435b3c255f417ad1722250faaf006c66b9090207f66 in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:1cc3d825d8b2468ef662a8b631220516f492e24232477209fe863836d2d2ed44`  
		Last Modified: Fri, 06 Sep 2024 22:20:59 GMT  
		Size: 3.4 MB (3416313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb34bac3028cbd14c26d70ad33e54a8a81eaae1cb9f77e3d0480cd8ae94edc27`  
		Last Modified: Fri, 06 Sep 2024 23:25:44 GMT  
		Size: 41.6 MB (41599498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:190539f673ac5ecc35ce0251463ff26d48c76bafbd8bf5aa8cbfed37c9cc19da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.2 KB (193180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:514667510d01b85b201eaa86aa416c8e84ddcd3b09d0977527151089af7e66d5`

```dockerfile
```

-	Layers:
	-	`sha256:e5d8a083575e7544b05235e25fa93119c0cbc014b19791565cc9fc0349c922d6`  
		Last Modified: Fri, 06 Sep 2024 23:25:43 GMT  
		Size: 184.7 KB (184726 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83e04c0497f233332eb43ae4fa61a6189891d482458920d04f1384c94b6d5d17`  
		Last Modified: Fri, 06 Sep 2024 23:25:43 GMT  
		Size: 8.5 KB (8454 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:d149d906102a9cb0cc2e7cff5c1448779065ec05ecc75138480b94f5c21d4624
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44645974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f16a6218b5d15cd0816e543880077a4cc6202ee9f015e7e7a9c6dee16e37e0f`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:4a10978248445fe045fc2859ce867988ab71bd2281ad7d88b62597252642a56b in / 
# Tue, 16 Jul 2024 22:56:42 GMT
CMD ["/bin/sh"]
# Tue, 16 Jul 2024 22:56:42 GMT
ARG version=8.422.05.1
# Tue, 16 Jul 2024 22:56:42 GMT
# ARGS: version=8.422.05.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Tue, 16 Jul 2024 22:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 16 Jul 2024 22:56:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:4983c3fe2029a430985943e6d87b35248366efd28cee655acc3ebff5daf703fa`  
		Last Modified: Mon, 22 Jul 2024 21:44:57 GMT  
		Size: 3.3 MB (3339494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3879fc1f7aaa8334f9a89f30e42d88048e377e5abd153683d682129aab974d2e`  
		Last Modified: Wed, 24 Jul 2024 10:38:10 GMT  
		Size: 41.3 MB (41306480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:27ebeed300303ef8f542a25b5cb3fd455589a7893f71cd6999955e4e457fc3a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3ad2d78c6ed8ac73a88795758a7427383a4a660d9c05ebca1a149ba9813bd2`

```dockerfile
```

-	Layers:
	-	`sha256:a315dc740d6d088fc6a30460105b18b22bc481f74a5da85d1cae02a5c63aa46a`  
		Last Modified: Wed, 24 Jul 2024 10:38:09 GMT  
		Size: 184.8 KB (184834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbdea74ffe3639d13fdb8fb9f6c8158964509d59dc2a92b43abe93d880f7f99a`  
		Last Modified: Wed, 24 Jul 2024 10:38:09 GMT  
		Size: 8.7 KB (8729 bytes)  
		MIME: application/vnd.in-toto+json
