## `amazoncorretto:11-alpine3.19-jdk`

```console
$ docker pull amazoncorretto@sha256:2e6b5cbffbf0a1c1f90c13cb5d6fd8a7121ba000fb26fa7e387e12d7eb9725e1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:11-alpine3.19-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8261dd092f48c98f65e568a3be871942cdf7acaf5d97c3dfc15cf0468fd935f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **145.5 MB (145490152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:418fa72b614755d5d4c20fcd5531d755de179355f81c67da1e21a3e0229be365`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30453e2a9661a1ae2955494e3301f6e248a60b9695bd63a10d12ad32d04971d8`  
		Last Modified: Wed, 08 Oct 2025 22:59:26 GMT  
		Size: 142.1 MB (142070337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:7b776e7b611f0d783697acaf8fe94be3e32c7459a9778aff4c76c8ad8a9100f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.7 KB (398703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7484685ac92433651c5fe73a0ad539bd440a9d2631004f023eda5a94ae3a3545`

```dockerfile
```

-	Layers:
	-	`sha256:6f9e65cf4d342d3f5f48ecdc1209fb682f1cd494138be799264eb79929a487c9`  
		Last Modified: Thu, 09 Oct 2025 00:47:34 GMT  
		Size: 389.3 KB (389286 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2733490300a07743934be2bc01c2d253b3e1f0254dbb04868652989ddf76e878`  
		Last Modified: Thu, 09 Oct 2025 00:47:35 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:11-alpine3.19-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:f95ba5ed29b97c0a77ca6d75aede9764affdf6350024dd0b55dea29c7f6bb1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **143.6 MB (143601040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fc7e29872eabb9154121e67e58d3fbf3f5908afbc8c78b316b630f64cbc6994`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=11.0.28.6.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=11.0.28.6.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0 &&     rm -rf /usr/lib/jvm/java-11-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 17 Sep 2025 00:23:53 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a3e27cc9dcb714859b79d4e669cf49ee62e5337d69a831c563552424905b66`  
		Last Modified: Thu, 09 Oct 2025 01:13:49 GMT  
		Size: 140.2 MB (140241739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:11-alpine3.19-jdk` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:f0259346827517a9eee6b0a353ab442be75c7741c1e8cd9e6bf851264ff4f817
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **398.9 KB (398863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5506628fce081edbe5d6082b6d8ad0c957f5dec6a2021b962902769765f355c`

```dockerfile
```

-	Layers:
	-	`sha256:d8f95ff703e27404628008462fd8d3e2833374af7c75a955be4871b2d4db16ad`  
		Last Modified: Thu, 09 Oct 2025 00:47:38 GMT  
		Size: 389.3 KB (389342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97b89450658e818dc2c9a40d018ab5ce83b3993e9f17a385e1869a317930470a`  
		Last Modified: Thu, 09 Oct 2025 00:47:39 GMT  
		Size: 9.5 KB (9521 bytes)  
		MIME: application/vnd.in-toto+json
