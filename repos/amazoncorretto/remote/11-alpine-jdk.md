## `amazoncorretto:11-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:217380c84c71bf4c2c50d1bdb88b43799739e0926c4e789bfcde6a2868b2acce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `amazoncorretto:11-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:a5969c0cbb2f535fb9805458521b92e367b7e0892332c1a1ec154e1cb9f3967a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.1 MB (195086937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad73cd324613512fd641af891f73bfd96f049fa10f5e12bd6a8566227052d843`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Thu, 18 Mar 2021 01:20:17 GMT
ARG version=11.0.10.9.1
# Thu, 18 Mar 2021 01:20:42 GMT
# ARGS: version=11.0.10.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 18 Mar 2021 01:20:43 GMT
ENV LANG=C.UTF-8
# Thu, 18 Mar 2021 01:20:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 18 Mar 2021 01:20:43 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d953de568d758f68db7c3d2239524e4f5915c33e8bea10ade61793e071c274d`  
		Last Modified: Thu, 18 Mar 2021 01:24:48 GMT  
		Size: 192.3 MB (192287444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
