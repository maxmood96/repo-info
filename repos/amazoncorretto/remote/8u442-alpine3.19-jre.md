## `amazoncorretto:8u442-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:d6a23df017d57508f747263a4bccebf6b7856346104f31b190e4bb9899f75408
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u442-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8f15c0e38ba58427e697392d39d5594bee629b80181acf2e4028287578915cd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.1 MB (45075311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6088130d49151f04ef65100ecd7f1292194cf7631384c00db0215bcdff1321d6`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 24 Jan 2025 20:03:54 GMT
ADD alpine-minirootfs-3.19.7-x86_64.tar.gz / # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2025 20:03:54 GMT
ARG version=8.442.06.1
# Fri, 24 Jan 2025 20:03:54 GMT
# ARGS: version=8.442.06.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Fri, 24 Jan 2025 20:03:54 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2025 20:03:54 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:83abf496f1b833f01c8f72695520b8975cc8b730d14a8ac270d6201bd0f1877e`  
		Last Modified: Fri, 14 Feb 2025 14:30:10 GMT  
		Size: 3.4 MB (3420868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73e6bef2d1123cd06f9d330dfa49f8772ff85bd08ee90938eca0ee1b25a7b80`  
		Last Modified: Fri, 14 Feb 2025 19:12:08 GMT  
		Size: 41.7 MB (41654443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:39e6a0192c63cfb7c3f1738e83396679ee3df856225e279056d11ae19a437a83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.0 KB (194030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bc0ab87952782a7bc803507d48f22b22968ee4c7ea28b975aa0c285ea3ffbb5`

```dockerfile
```

-	Layers:
	-	`sha256:1277f8057587f5ab410813aeb87580f309dabe57032d8ebdd4f3e5747ae7e895`  
		Last Modified: Fri, 14 Feb 2025 22:50:02 GMT  
		Size: 185.3 KB (185331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:129a80fce2d6777f3f90e24848fc4dc63b1fd37ba976e74e4c739b20abacd6ab`  
		Last Modified: Fri, 14 Feb 2025 22:50:03 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u442-alpine3.19-jre` - linux; arm64 variant v8

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
		Last Modified: Tue, 14 Jan 2025 20:33:05 GMT  
		Size: 3.4 MB (3360532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92638f98fc5a8af1f2ab561120f8b79ed60affc1f30e3cf43b5b932bf61ed07e`  
		Last Modified: Tue, 04 Feb 2025 06:52:51 GMT  
		Size: 41.4 MB (41362327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u442-alpine3.19-jre` - unknown; unknown

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
		Last Modified: Fri, 14 Feb 2025 22:50:04 GMT  
		Size: 185.4 KB (185439 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18bf696667b3e712bfdd2c953679e61978cbc843f0a85d6b557348bf050465e9`  
		Last Modified: Fri, 14 Feb 2025 22:50:04 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
