## `amazoncorretto:11-alpine3.12-jdk`

```console
$ docker pull amazoncorretto@sha256:c99192a77975e33850f7a0d0d47a37173dac9354730d649b50ccb9ddbe8cbeff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:11-alpine3.12-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:e617b7d6790ee8a6f058013eab4d30b21e0ad723d3b554069cc96820e272577c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.3 MB (196267606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74c9834b09b550397945526d1f0ae95630b0de38ddf9b92f7116404d5809fcf2`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 15:19:45 GMT
ADD file:cdff961a4dd899295df5fd92711f8ee8fd8e682208d52bcfcfa3fcffd295821f in / 
# Thu, 17 Mar 2022 15:19:45 GMT
CMD ["/bin/sh"]
# Sat, 19 Mar 2022 00:36:03 GMT
ARG version=11.0.14.9.1
# Sat, 19 Mar 2022 00:36:16 GMT
# ARGS: version=11.0.14.9.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Sat, 19 Mar 2022 00:36:16 GMT
ENV LANG=C.UTF-8
# Sat, 19 Mar 2022 00:36:17 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 19 Mar 2022 00:36:17 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c7f02851fb7d4b5eb2cdd31353ecdcfc954d48241f12bbe91b831f73abe2d29c`  
		Last Modified: Thu, 17 Mar 2022 15:20:34 GMT  
		Size: 2.8 MB (2806202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d133b7ab11d6f67ecf110a25590802ce5b4d4ed8da214dda7ae8323ba3570b3c`  
		Last Modified: Sat, 19 Mar 2022 00:43:44 GMT  
		Size: 193.5 MB (193461404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
