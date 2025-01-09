## `amazoncorretto:8u432-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:77911845eecfaa5f0c432f3115eb6e3765b0110d2b3af94483be3fdf4e947db1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u432-alpine3.19-jre` - linux; amd64

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

### `amazoncorretto:8u432-alpine3.19-jre` - unknown; unknown

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

### `amazoncorretto:8u432-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:9310bbdde7da03f62d28e2eff18179c76cc69172f5f6e55ed7990030a48b934a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.7 MB (44710489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f18ff17ad84deff167009e01ccc8e212b2666d9ef8ae310b9382b6bd9939bc4`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 13 Dec 2024 23:01:14 GMT
ADD alpine-minirootfs-3.19.5-aarch64.tar.gz / # buildkit
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
	-	`sha256:f2178dde0fb65be0d15359886bb642d5d8dac86ca2d709ab90f8f0ee62211ca2`  
		Last Modified: Tue, 07 Jan 2025 03:03:15 GMT  
		Size: 3.4 MB (3351948 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd44d72afbc586cbf39ec229e15563edf90845ba9e5b3b65e16add03bb72f102`  
		Last Modified: Tue, 07 Jan 2025 07:20:09 GMT  
		Size: 41.4 MB (41358541 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u432-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4ce546a60dae6137a39b3ba45328be6b073445308b2b0e76b9bbb3ca344c4217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.2 KB (194218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc6e613c567e395deb9c2790f6059aac29373416a9554e029d4cfa42f3a138b3`

```dockerfile
```

-	Layers:
	-	`sha256:811caef74cbecfb960a8dda700bea156f24562fe9e4832d4293fc564498e1457`  
		Last Modified: Tue, 07 Jan 2025 07:20:07 GMT  
		Size: 185.4 KB (185439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f580a2dd84891a46b789b05213b39078222571bdb72cf6e38bd595941eef0f8`  
		Last Modified: Tue, 07 Jan 2025 07:20:07 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
