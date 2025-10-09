## `amazoncorretto:8u462-alpine3.19-jre`

```console
$ docker pull amazoncorretto@sha256:334bf0ef4c27b8bd5f153eeaeb8cb3d9feb517253901d7352fe5024b9dcce537
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8u462-alpine3.19-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0f028e2b0d574bb4da80fbc8f6b9f52f33dee4faf9f07cb1a48a7652f4f4aead
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45151376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbe360e149a2a3fb3d0ff529ec0ccf17706e6e8e9f3bf760d656b09d585cec35`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-x86_64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:17a39c0ba978cc27001e9c56a480f98106e1ab74bd56eb302f9fd4cf758ea43f`  
		Last Modified: Wed, 08 Oct 2025 12:04:11 GMT  
		Size: 3.4 MB (3419815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b49d07ea50ad4a71059037c5d37b6f0d40ff836da0987050d83027b5fa906d7b`  
		Last Modified: Wed, 08 Oct 2025 22:59:06 GMT  
		Size: 41.7 MB (41731561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:a1840afd1eaf52fa6455f74ce6e1d33ec0f64ce3a1f79fbc556c4c5054e15fef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.8 KB (195800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7851f9da8dbc30fe632ee1a9535c562871797db07c92461ace3e3785ae01e9b0`

```dockerfile
```

-	Layers:
	-	`sha256:38da57d2c10f2d4325811d46520524acedad5c067100c3059e82a8bd2e21fb7c`  
		Last Modified: Thu, 09 Oct 2025 00:53:21 GMT  
		Size: 187.1 KB (187101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b794eae928ed134ed6a1930438fc9b15d462fe014b4163797c27d57a789437ae`  
		Last Modified: Thu, 09 Oct 2025 00:53:21 GMT  
		Size: 8.7 KB (8699 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8u462-alpine3.19-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:78acc6f64a52c0a7379aaf611466d584f227177a8459bde43d2b03a2d7d2b5b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44796268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d14cc3f20a823ac053eb7efd13dcbae3e4a443c5392b9640871a974872d0b20e`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.19.9-aarch64.tar.gz / # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
CMD ["/bin/sh"]
# Wed, 17 Sep 2025 00:23:53 GMT
ARG version=8.462.08.1
# Wed, 17 Sep 2025 00:23:53 GMT
# ARGS: version=8.462.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0 &&     rm -rf /usr/lib/jvm/java-8-amazon-corretto/lib/src.zip # buildkit
# Wed, 17 Sep 2025 00:23:53 GMT
ENV LANG=C.UTF-8
# Wed, 17 Sep 2025 00:23:53 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:5711127a7748d32f5a69380c27daf1382f2c6674ea7a60d2a3e338818590fea1`  
		Last Modified: Wed, 08 Oct 2025 12:04:21 GMT  
		Size: 3.4 MB (3359301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e07529482cedae07b41556edf4efac6fb631b56bacb5d4932174a87308fd636f`  
		Last Modified: Wed, 08 Oct 2025 21:46:13 GMT  
		Size: 41.4 MB (41436967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8u462-alpine3.19-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:eb4044cfc0014a0cb9a6102cd67ba788d9057a3eb30ecf073e8ed76c21642183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.0 KB (195987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a87b19607719e8416d3634aa8cae17dd3a02d61080e3c50bade7c2084fd2d07`

```dockerfile
```

-	Layers:
	-	`sha256:a395b9bf506a868b55a056a5947761896ee68be34eb36a4291eadd7eb6246d7a`  
		Last Modified: Thu, 09 Oct 2025 00:53:25 GMT  
		Size: 187.2 KB (187209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2663840e755ed14687c2bbf1df07aa6f2a8659cf59c14fe5deb26ed4c3aea1`  
		Last Modified: Thu, 09 Oct 2025 00:53:25 GMT  
		Size: 8.8 KB (8778 bytes)  
		MIME: application/vnd.in-toto+json
