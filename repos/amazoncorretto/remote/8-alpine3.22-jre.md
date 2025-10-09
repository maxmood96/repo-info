## `amazoncorretto:8-alpine3.22-jre`

```console
$ docker pull amazoncorretto@sha256:075746a0e83ea8376ab07aacf6ef097373f60fd250d85f95d9b501fca69edf36
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:8-alpine3.22-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8a7cbb4280c1c8a5dd63f10e4c526b8b42a459f4ff8a8aec3b334c6126c7ee4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45533370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77c5e4b4e3ad3bac73a139e1785d61399ddfc49f8840850c08dd1a2d038766d3`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
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
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d126c1f45f7e898ca33c4cd138c31bbc223bfe7f6aecafd0fab266b96aa5138`  
		Last Modified: Wed, 08 Oct 2025 22:59:23 GMT  
		Size: 41.7 MB (41730918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:e08ede9b7d6942459fffbaafb7a46454aa1156eeeffc58c1835d869f48d5d96f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.4 KB (198384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65dff62d6e3171cae1a5a5345523eb712e8e3a092c1d70db2c7912fdd70deb3e`

```dockerfile
```

-	Layers:
	-	`sha256:464ec38bd6376416695bb5a8a0deaea15395ce2699f93aff6aebc7fe48f1fab5`  
		Last Modified: Thu, 09 Oct 2025 00:53:03 GMT  
		Size: 189.0 KB (189026 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b1df2955a36b1f37634124eb46d9621fc24da919b7a119f8e4d9b1f641ac6d4`  
		Last Modified: Thu, 09 Oct 2025 00:53:04 GMT  
		Size: 9.4 KB (9358 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:8-alpine3.22-jre` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:614628006243fe38c03e48a0fc91f45520d2cf71ef0c36f4c0cbf4922aa11901
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45570224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b8f098caed4bc2a8afe8125a4009e710daad658d4f39a89ced58f70d723338`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 17 Sep 2025 00:23:53 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
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
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Wed, 08 Oct 2025 12:04:34 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fba3d99d4f0a99d2d3b8fcb4a87c224e8898eb4302559a074d98936a89c99eb`  
		Last Modified: Wed, 08 Oct 2025 21:46:35 GMT  
		Size: 41.4 MB (41432155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:8-alpine3.22-jre` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:48813286cbb0a2c252617d427d56e7b17cf6aa07f74b93cb00e41aee151f7e30
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 KB (198621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:913c9d6b1983860a994707cfcd0e362116f3f921220d5a1d2672413c750544f4`

```dockerfile
```

-	Layers:
	-	`sha256:a058a6a439de05ed8a5579e79f6385f8d6124f6751ba02f2871bd672130e2713`  
		Last Modified: Thu, 09 Oct 2025 00:53:07 GMT  
		Size: 189.2 KB (189158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3d0d95a2dc4ed32d9fa4e9c24050a970b797b69613dacaed652b3366744abb`  
		Last Modified: Thu, 09 Oct 2025 00:53:08 GMT  
		Size: 9.5 KB (9463 bytes)  
		MIME: application/vnd.in-toto+json
