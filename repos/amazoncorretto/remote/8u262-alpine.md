## `amazoncorretto:8u262-alpine`

```console
$ docker pull amazoncorretto@sha256:efa8c42d9e070114e17291941bc555e3649f4e5b31e70282b5e9483035c2a5cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u262-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:5bed8fd35066096b34cd5079305b240912a5c742f034f0a44707ca9d7a7ea561
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **100.8 MB (100775653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa3742ee1ff840f4683087f0e6e478f20bf2af22f34ea6bb0ff202336278145`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Wed, 26 Aug 2020 18:19:51 GMT
ARG version=8.265.01.2
# Wed, 26 Aug 2020 18:19:56 GMT
# ARGS: version=8.265.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar xvzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Wed, 26 Aug 2020 18:19:56 GMT
ENV LANG=C.UTF-8
# Wed, 26 Aug 2020 18:19:57 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 26 Aug 2020 18:19:57 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d07d0b0a5d754b81997a849b30240767842e1115835c2355bd933b6f90f03397`  
		Last Modified: Wed, 26 Aug 2020 18:20:42 GMT  
		Size: 98.0 MB (97978112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
