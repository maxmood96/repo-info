## `amazoncorretto:19-alpine3.14-jdk`

```console
$ docker pull amazoncorretto@sha256:f021cf535192f8f1533e56f6c209201598b74dc58f42a31bb90f6e19b5d17d11
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine3.14-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:0b6118d4859ee5b9d6ed54d53abdd927b0dad16fa2ac97b857d7905698e0580d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.9 MB (204916900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1db5e8a2ca165f4f9af728d523c8f58364ada3b7ac8777468deda2e9e5abf808`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:19:12 GMT
ARG version=19.0.2.7.1
# Wed, 29 Mar 2023 19:19:18 GMT
# ARGS: version=19.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Wed, 29 Mar 2023 19:19:18 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 19:19:18 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 29 Mar 2023 19:19:18 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b9e24612246fce09a18470839ef6c07650a2eea3592d5b9d77b5badb24f564c`  
		Last Modified: Wed, 29 Mar 2023 19:27:52 GMT  
		Size: 202.1 MB (202087253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
