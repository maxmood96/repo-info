## `amazoncorretto:17-alpine3.14`

```console
$ docker pull amazoncorretto@sha256:ce8b19cb9029fc6fb25cecf601fb6ba3779d7c87998fa8a1a5e99b5c1080a484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.14` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:34df0f628473bc0b0c5424e6ef809a5083b06b88bcf9843ced2a14deb2f922bf
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.4 MB (196398954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2897450068e4928b3e89cc43882224b8e5e4081aa99bb10f9a1d6b115ad837`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:18:38 GMT
ARG version=17.0.6.10.1
# Wed, 29 Mar 2023 19:18:43 GMT
# ARGS: version=17.0.6.10.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Wed, 29 Mar 2023 19:18:43 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 19:18:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 29 Mar 2023 19:18:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f5239bf69b2f79c92daf65f391f771f5783fed6f3972d5ce025c460ab92dda`  
		Last Modified: Wed, 29 Mar 2023 19:25:59 GMT  
		Size: 193.6 MB (193569307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
