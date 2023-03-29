## `amazoncorretto:8-alpine3.14-jre`

```console
$ docker pull amazoncorretto@sha256:f39159428c8726df74ee6d76e990c643f47bcb72ea15831b62a74dfd1148f355
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.14-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:70e511ce0ebf473d2b8eb875c8a5092817fbaecb36f70af6610daf8cdfb70b2b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44364639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf326f7e9ae00faafdfdbd972b7697d9431f890917b7304cf6c2d324c801debd`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:17:05 GMT
ARG version=8.362.08.1
# Wed, 29 Mar 2023 19:17:14 GMT
# ARGS: version=8.362.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Wed, 29 Mar 2023 19:17:15 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 19:17:15 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f95b7bbba50a7b2ffda26c2fa90f4d5fa10c0f942490cc969e91fa52dece9ce`  
		Last Modified: Wed, 29 Mar 2023 19:21:48 GMT  
		Size: 41.5 MB (41534992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
