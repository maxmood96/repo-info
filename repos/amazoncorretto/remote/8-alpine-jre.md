## `amazoncorretto:8-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:321b72fc01814df87a5c8ad2037ddd827c24104ba02ad1243b10976d3ccddd09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:fd4d9639049a514b208332b987707c2a30d99d37d5de495a0d9c7ec791b4b5f2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43199380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dbd9d0a28efc5a6e6a8e9402cda63ff0f6594b632c6dc7fffd592ef87c0d590`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Nov 2021 20:19:40 GMT
ADD file:9233f6f2237d79659a9521f7e390df217cec49f1a8aa3a12147bbca1956acdb9 in / 
# Wed, 24 Nov 2021 20:19:40 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:02:51 GMT
ARG version=8.322.06.2
# Wed, 19 Jan 2022 22:03:02 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Wed, 19 Jan 2022 22:03:02 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:03:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:59bf1c3509f33515622619af21ed55bbe26d24913cedbca106468a5fb37a50c3`  
		Last Modified: Wed, 24 Nov 2021 20:20:05 GMT  
		Size: 2.8 MB (2818413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec8108044b2feaadcace7f8f0ed207b3fafe303a3ef4ad27d4721592c9cc874`  
		Last Modified: Wed, 19 Jan 2022 22:10:00 GMT  
		Size: 40.4 MB (40380967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
