## `amazoncorretto:8-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:d8aa6f87d43ce38408664a18a7a2241286a288c9f74e0ce875b5a97eac451b66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:6e78baa973911d10c4431d49c5aed6adb8a89cb3c4f1aef92dae795b8e4498b9
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42196224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad09a6cff848a0c03ad96959d41152aa3183adf72cb4db3a6e547a90bb30920`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Wed, 26 Aug 2020 18:19:51 GMT
ARG version=8.265.01.2
# Wed, 26 Aug 2020 18:20:04 GMT
# ARGS: version=8.265.01.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar xvzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Wed, 26 Aug 2020 18:20:04 GMT
ENV LANG=C.UTF-8
# Wed, 26 Aug 2020 18:20:05 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06093dd7a755228d11dcf1d13c01872a5f44f8d31ae2cbab7f1fc7c4e1f1a6be`  
		Last Modified: Wed, 26 Aug 2020 18:20:53 GMT  
		Size: 39.4 MB (39398683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
