## `amazoncorretto:18-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:4636769abd5d04c2417d39590a1c5a7d732642cf1682605d388a891d7af2e9d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:18-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:16ff5a1f7b4d0cefc8c7cc5a6897d0a1b6fff6dc8a2e8602db226c6c2f63c354
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **195.7 MB (195667087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc7f67737535c8e140ba32c5b98662ea25525f3eedfa7ba8f3d0c1adf7c67a0d`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Sep 2022 21:20:49 GMT
ARG version=18.0.2.9.1
# Wed, 28 Sep 2022 21:20:55 GMT
# ARGS: version=18.0.2.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-18=$version-r0
# Wed, 28 Sep 2022 21:20:55 GMT
ENV LANG=C.UTF-8
# Wed, 28 Sep 2022 21:20:55 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 28 Sep 2022 21:20:56 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c769a0a2b3574d61da3f4d7f04b2dae80c6369a3ad8c358341b0badf992165dd`  
		Last Modified: Wed, 28 Sep 2022 21:26:11 GMT  
		Size: 192.9 MB (192861033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
