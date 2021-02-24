## `amazoncorretto:15-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:d89b97919bbce80a222355a6ad068f7e790d4ba674d58e900b80b14f45b853f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8910639d896f1882a0ef660c0d168a1232d8d46186f8ef82c1071c200ef680dd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207723372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b2b8f7624cc0379a6e3ce956ba4f52f071775aa9e534f78f4a4126a8f31c707`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:56:44 GMT
ARG version=15.0.2.7.1
# Wed, 24 Feb 2021 20:56:51 GMT
# ARGS: version=15.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Wed, 24 Feb 2021 20:56:52 GMT
ENV LANG=C.UTF-8
# Wed, 24 Feb 2021 20:56:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 24 Feb 2021 20:56:52 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f6d2a68570ac40a139537046b9da75ef1988c6ca97fcffa8acd7783e70b2b3`  
		Last Modified: Wed, 24 Feb 2021 20:58:36 GMT  
		Size: 204.9 MB (204923879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
