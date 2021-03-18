## `amazoncorretto:15-alpine-full`

```console
$ docker pull amazoncorretto@sha256:4b38c5c2a4d87ae1a9ecbf3375087824295a5db316f19c760da08b679cd1591e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:15-alpine-full` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:8f82bafee561f23a4f672d60ab517f5ba3eefbd3dfa9259c0e49b16578e98614
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.7 MB (207723406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d987e512ca1046e02b2589a41277f2f3a87aeb4cd72ee81910b67791c74f469`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Thu, 18 Mar 2021 01:21:10 GMT
ARG version=15.0.2.7.1
# Thu, 18 Mar 2021 01:21:16 GMT
# ARGS: version=15.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-15=$version-r0
# Thu, 18 Mar 2021 01:21:17 GMT
ENV LANG=C.UTF-8
# Thu, 18 Mar 2021 01:21:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 18 Mar 2021 01:21:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:179568b81de52af0559ed75a7c6c8f6ff175084c871df9f6ca44c4e687328419`  
		Last Modified: Thu, 18 Mar 2021 01:25:58 GMT  
		Size: 204.9 MB (204923913 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
