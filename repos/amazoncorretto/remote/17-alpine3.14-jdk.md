## `amazoncorretto:17-alpine3.14-jdk`

```console
$ docker pull amazoncorretto@sha256:fa1de2a0a4382ea5af15aae71b6e46ca3a2a927042fd0de3851455c6f6fbb152
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:17-alpine3.14-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:2967844bd2f73589f13802538dca6a8e3a7959ea20eb2cc87cf249a4bfd28719
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194637385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538a73bfad111e73a55790fb4c956118e4b2df065f57e59d637c8e6ccc08d25c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:05:13 GMT
ARG version=17.0.2.8.1
# Wed, 19 Jan 2022 22:05:22 GMT
# ARGS: version=17.0.2.8.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-17=$version-r0
# Wed, 19 Jan 2022 22:05:22 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:05:23 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jan 2022 22:05:23 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d1020dd57bec29a0da6f43465c198c3c0c326f6e78e6d7fcf06f0a6cc26c6de`  
		Last Modified: Wed, 19 Jan 2022 22:17:29 GMT  
		Size: 191.8 MB (191814404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
