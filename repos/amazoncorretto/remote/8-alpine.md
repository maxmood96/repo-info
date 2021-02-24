## `amazoncorretto:8-alpine`

```console
$ docker pull amazoncorretto@sha256:03b349394264852d89b5f7cda9875ccde0481758f0a7e8fbe3d5a6bf6e79b104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:8-alpine` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:3628bdc6ea26a18523be8b6558a6a48c0b1b16cc61a094494206964c3ab4c850
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.8 MB (101783805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5341e57e8e4184948d22f6fc5a5df65cebc1142ded61b41a9d69c6a73ad5ea68`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:56:07 GMT
ARG version=8.282.08.1
# Wed, 24 Feb 2021 20:56:11 GMT
# ARGS: version=8.282.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Wed, 24 Feb 2021 20:56:12 GMT
ENV LANG=C.UTF-8
# Wed, 24 Feb 2021 20:56:12 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 24 Feb 2021 20:56:12 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:368ffdd1bfbcddc2e0c21c4443db268837bb5a359e7dd87dd7193dff8478849f`  
		Last Modified: Wed, 24 Feb 2021 20:57:32 GMT  
		Size: 99.0 MB (98984312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
