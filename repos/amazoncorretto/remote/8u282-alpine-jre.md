## `amazoncorretto:8u282-alpine-jre`

```console
$ docker pull amazoncorretto@sha256:dceea08de1026fa25c7fc0e3303a0f028e2f366ef2f4b3ed179670f03db03abc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8u282-alpine-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:1f3cb1ebbc8b142e521accee2cb8216c49aa6a4deb36e0e4a738c16ce3b5d589
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43115484 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4319df2556256d87c9c8aa95e6b0481169fe76b74a7a2ee1603d7194a90825a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Thu, 18 Mar 2021 01:20:03 GMT
ARG version=8.282.08.1
# Thu, 18 Mar 2021 01:20:14 GMT
# ARGS: version=8.282.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Thu, 18 Mar 2021 01:20:14 GMT
ENV LANG=C.UTF-8
# Thu, 18 Mar 2021 01:20:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9437530167249f5bfdbaa8012d069e8ad03ca434d123dd810aa25978e8469c22`  
		Last Modified: Thu, 18 Mar 2021 01:24:17 GMT  
		Size: 40.3 MB (40315991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
