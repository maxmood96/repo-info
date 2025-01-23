## `amazoncorretto:8-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:1864cc54b0e7607b07b74b523fd8f36bc4f962155c687ce25a3ef13372e73956
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:91bfa185c82c116f53f031150cd8b89297f9f0d79e3c338dd7b850d89c097508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45075842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4473b9597bd12dd5a86092e658a2bd80b2c250febac618ddb67085a0b6cb5233`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.6-x86_64.tar.gz / # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
CMD ["/bin/sh"]
# Fri, 13 Dec 2024 23:01:14 GMT
ARG version=8.432.06.1
# Fri, 13 Dec 2024 23:01:14 GMT
# ARGS: version=8.432.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 13 Dec 2024 23:01:14 GMT
ENV LANG=C.UTF-8
# Fri, 13 Dec 2024 23:01:14 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:861950bce9fa55e0462bb22503f61d8e7396f292af10969506b51e7bdb701d60`  
		Last Modified: Wed, 08 Jan 2025 17:23:45 GMT  
		Size: 3.4 MB (3420242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9e18b1919670bced50c3ea12cad4b07ea034179c06a05becd618ca5e84e860`  
		Last Modified: Wed, 08 Jan 2025 18:09:37 GMT  
		Size: 41.7 MB (41655600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:628a17712ef00fc6568ef9c0980af23501560be8c95a06edca75e6b739c6f238
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 KB (194030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90f3b0caa52a013bfcce6a6c8d92e75756fb5a5aed32f54eb4cfae44abceecdd`

```dockerfile
```

-	Layers:
	-	`sha256:b1ac9d284bf9077cb29f4533c7fd0711854dbda3283d699cf6a2d8d42472acf7`  
		Last Modified: Wed, 08 Jan 2025 18:09:36 GMT  
		Size: 185.3 KB (185331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52b17e018040ddea80581307860c9ee11f99bea5b0706e347145989b9764690e`  
		Last Modified: Wed, 08 Jan 2025 18:09:35 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9088d72fd8ab9fd43fb2ed0896d503cfbbc43fc53a8df31083ecdbea679ee034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44722859 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d093633200534ce2cb0c4870be00ff0388a9068370f97408f52597ea45c83d4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 08 Jan 2025 12:06:42 GMT
ADD alpine-minirootfs-3.19.6-aarch64.tar.gz / # buildkit
# Wed, 08 Jan 2025 12:06:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2025 01:09:23 GMT
ARG version=8.442.06.1
# Thu, 23 Jan 2025 01:09:23 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Thu, 23 Jan 2025 01:09:23 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2025 01:09:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:88b83b407e415cb5cb78776f0e83bf403b89f77eb02721ce6a3cbf1eba723438`  
		Last Modified: Wed, 08 Jan 2025 17:24:18 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92638f98fc5a8af1f2ab561120f8b79ed60affc1f30e3cf43b5b932bf61ed07e`  
		Last Modified: Thu, 23 Jan 2025 18:33:09 GMT  
		Size: 41.4 MB (41362327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:6dfd12027bfe5cacbf2b5210f110a19aba53258b68ce92e4276ea1139868a687
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4db30d40f1514ec4ac17c646ae27dfe5ca4b871de4f5740e74b12dfb3b382b7e`

```dockerfile
```

-	Layers:
	-	`sha256:701703987e890f4b002552e6b3d3852f22a623745368945b48cc3cf73ae86ec2`  
		Last Modified: Thu, 23 Jan 2025 18:33:08 GMT  
		Size: 185.4 KB (185439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18bf696667b3e712bfdd2c953679e61978cbc843f0a85d6b557348bf050465e9`  
		Last Modified: Thu, 23 Jan 2025 18:33:08 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
