## `amazoncorretto:8u352-alpine3.16-jre`

```console
$ docker pull amazoncorretto@sha256:68af66a13a5d3fd46b00a19c16f3b3261e42193efbf39232e33f14ad9539b002
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u352-alpine3.16-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:153a5cfb49dc5cd87565f72e800f299c9e341751193ae3a7dafa7a7736ac97c6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43243222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:423634d0bef57962200f0332354b716c36ed708a44a9c60798116b41dea2059a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 12 Nov 2022 04:19:23 GMT
ADD file:ceeb6e8632fafc657116cbf3afbd522185a16963230b57881073dad22eb0e1a3 in / 
# Sat, 12 Nov 2022 04:19:23 GMT
CMD ["/bin/sh"]
# Sat, 12 Nov 2022 04:35:40 GMT
ARG version=8.352.08.1
# Sat, 12 Nov 2022 04:35:52 GMT
# ARGS: version=8.352.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Sat, 12 Nov 2022 04:35:52 GMT
ENV LANG=C.UTF-8
# Sat, 12 Nov 2022 04:35:52 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:ca7dd9ec2225f2385955c43b2379305acd51543c28cf1d4e94522b3d94cce3ce`  
		Last Modified: Sat, 12 Nov 2022 02:52:15 GMT  
		Size: 2.8 MB (2806272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c5e68b8d5348a52ea70cf435f74a2f8d2fd4a66a38ba399af9436c98b491f5`  
		Last Modified: Sat, 12 Nov 2022 04:39:40 GMT  
		Size: 40.4 MB (40436950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
