## `amazoncorretto:8-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:bfe47738be6a51795defe79235d852d10b39be0cc4fc6397b81731063ffa0ce3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:bb5a1d1b855f53a97325bd0db922f26c8145409abb96331160b2ee8c10d196dc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edeed981e5f07e9164c3c42ebafd71874cdbe73a5730135d39a90811fe74e3e1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Thu, 18 Mar 2021 01:20:03 GMT
ARG version=8.282.08.1
# Thu, 18 Mar 2021 01:20:07 GMT
# ARGS: version=8.282.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Thu, 18 Mar 2021 01:20:08 GMT
ENV LANG=C.UTF-8
# Thu, 18 Mar 2021 01:20:08 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 18 Mar 2021 01:20:08 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629a502b899c5e23c927794b3141991bc82aee81b1612af3d54a83ac6fbcd4e7`  
		Last Modified: Thu, 18 Mar 2021 01:23:56 GMT  
		Size: 99.0 MB (98984472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
