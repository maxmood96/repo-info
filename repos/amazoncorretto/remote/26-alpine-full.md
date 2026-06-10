## `amazoncorretto:26-alpine-full`

```console
$ docker pull amazoncorretto@sha256:25db7605a9f298e511b40a729c17af3e258523be1b7462113e2667eb13bed0c8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `amazoncorretto:26-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2b5b0fdb9354355f9141a07900c20503d163ace8a5b713dd6d6bd4ec78f2d028
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **188.8 MB (188823498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bf7c1c9025cab115574eb0b578f15e80be3c47ada68a9c5b292d4b01eb7f712`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:31 GMT
ADD alpine-minirootfs-3.24.0-x86_64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:31 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:16:08 GMT
ARG version=26.0.1.8.1
# Wed, 10 Jun 2026 20:16:08 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:16:08 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:16:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:16:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:9b70e313681f44d32991ec943f89228bc91d7431d4a84feafc269a76e3f96a63`  
		Last Modified: Tue, 09 Jun 2026 20:11:36 GMT  
		Size: 3.9 MB (3866755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48347521e1e1de9b0123f3fd4e2aae37fe7dbfb1e0665f4914a2059925ae251d`  
		Last Modified: Wed, 10 Jun 2026 20:16:28 GMT  
		Size: 185.0 MB (184956743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:bb2b1b80b9df1de563b464e7b7408eb0b0302d9b6fc2dfe2f254df18b2cd31d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **598.4 KB (598367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a2aa37826b876bf13c8a3077046f4af6079514821126c4c9930ea965fde5b2`

```dockerfile
```

-	Layers:
	-	`sha256:0d1b8c580ffb22b06d79020218d16dc54c8ecb59a437bc5ab71b57dcc0f7baf2`  
		Last Modified: Wed, 10 Jun 2026 20:16:24 GMT  
		Size: 587.7 KB (587690 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a8f2c210bd562b5c586731fbeaa1fbd430f91eaa5022dd2d9d71c159ac1febde`  
		Last Modified: Wed, 10 Jun 2026 20:16:24 GMT  
		Size: 10.7 KB (10677 bytes)  
		MIME: application/vnd.in-toto+json

### `amazoncorretto:26-alpine-full` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:22fefc148553578792d0594352adb114cc21c0dafee456c2fb1213712e7ac941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **186.7 MB (186722204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:674bf80cbe172358a868b0d1a9c287a9f12204adef434fc30cb1e124269f9dfb`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Jun 2026 20:11:09 GMT
ADD alpine-minirootfs-3.24.0-aarch64.tar.gz / # buildkit
# Tue, 09 Jun 2026 20:11:09 GMT
CMD ["/bin/sh"]
# Wed, 10 Jun 2026 20:15:49 GMT
ARG version=26.0.1.8.1
# Wed, 10 Jun 2026 20:15:49 GMT
# ARGS: version=26.0.1.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-26=$version-r0 &&     rm -rf /usr/lib/jvm/java-26-amazon-corretto/lib/src.zip # buildkit
# Wed, 10 Jun 2026 20:15:49 GMT
ENV LANG=C.UTF-8
# Wed, 10 Jun 2026 20:15:49 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 10 Jun 2026 20:15:49 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c05efffaed614b5ff4e3b9a80136e7c0eed0b47f434802c81baf254c0defca91`  
		Last Modified: Tue, 09 Jun 2026 20:11:14 GMT  
		Size: 4.2 MB (4202330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43148a393ecab6b545a9f156e4dda452958a384f3348165c0152b571508e88ba`  
		Last Modified: Wed, 10 Jun 2026 20:16:12 GMT  
		Size: 182.5 MB (182519874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `amazoncorretto:26-alpine-full` - unknown; unknown

```console
$ docker pull amazoncorretto@sha256:4173254e2381aaa0e0eded39457c6715ddbb01678c2aaf20a28aa5dbe374a8b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **597.3 KB (597333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b4a13b5e7f36fbf57001526966a803c07b6676bea3c79b5cd013609ecb0ae3`

```dockerfile
```

-	Layers:
	-	`sha256:38104777bc23d7b7dca24f057105ecefabcb8830bb1ba5bf90e3b4e2f1b47d56`  
		Last Modified: Wed, 10 Jun 2026 20:16:07 GMT  
		Size: 586.5 KB (586504 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c2b592d84ad907693ff15b5b4f09a5fa98fe894c9d6a29e36c87a93f9799ba49`  
		Last Modified: Wed, 10 Jun 2026 20:16:07 GMT  
		Size: 10.8 KB (10829 bytes)  
		MIME: application/vnd.in-toto+json
