## `amazoncorretto:8u422-alpine3.18-jre`

```console
$ docker pull amazoncorretto@sha256:c50dafcc0b215b3524b734bb861839d11975aa0d493f2530288b9464c4227650
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u422-alpine3.18-jre` - linux; amd64

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

### `amazoncorretto:8u422-alpine3.18-jre` - unknown; unknown

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

### `amazoncorretto:8u422-alpine3.18-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:ea2a4881814ee3e18a6b3d8c35f1fc4ef9305a98a18907e63898094922d89e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.6 MB (44646849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:218dfc169f49a574c8a8e208ca03f32a43372792f972473d823c15632c225ff2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 16 Jul 2024 22:56:42 GMT
ADD file:c2dbff469fced00345f9627d1efd892f94d53dbb31a6485fa9411b2fb1b4840f in / 
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
	-	`sha256:720f3032cd1105e6311c8adee3ee0f3b6827bec2c48f1cfff486a347ad22f05c`  
		Last Modified: Fri, 06 Sep 2024 22:44:58 GMT  
		Size: 3.3 MB (3340347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac151b7ace685d0ea481e525fe209aee22cf4e52d6dc2ae6db97dc3ee96cc75b`  
		Last Modified: Sat, 07 Sep 2024 12:06:25 GMT  
		Size: 41.3 MB (41306502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u422-alpine3.18-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:d92ac6564b2b89c574aa77f184c8d4d8ea92cfd0506f4d24271239b8062928d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **193.6 KB (193563 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8d60cdbf60adde5b14f0d0065bf4ed118e3c322ed02a3d37477cc0dc6aafe74`

```dockerfile
```

-	Layers:
	-	`sha256:a7013423e7a652c78eee7890e599444e7c940726e75e08801fc1765f1f2fd2cb`  
		Last Modified: Sat, 07 Sep 2024 12:06:23 GMT  
		Size: 184.8 KB (184834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79bf7ec42f97a1410d74bec9bb2fa425d4856af17cdc289dcf84add27e3a2a75`  
		Last Modified: Sat, 07 Sep 2024 12:06:23 GMT  
		Size: 8.7 KB (8729 bytes)  
		MIME: application/vnd.in-toto+json
