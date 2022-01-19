## `amazoncorretto:8-alpine3.14-jdk`

```console
$ docker pull amazoncorretto@sha256:42aa695a78f298d8d21df57ca86d387166115c245def688db8fe11bb6b2e683d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.14-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:231711bb7577e580933f9d234c710fd11d1f0b34c6a1f246ec7ad403bafe6238
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **101.9 MB (101926446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cad79a3a664e972af93336fae8c1051a89e4e54143d94047d8ac1a1971af98`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 19 Jan 2022 22:02:37 GMT
ARG version=8.322.06.2
# Wed, 19 Jan 2022 22:02:41 GMT
# ARGS: version=8.322.06.2
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Wed, 19 Jan 2022 22:02:42 GMT
ENV LANG=C.UTF-8
# Wed, 19 Jan 2022 22:02:42 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 19 Jan 2022 22:02:42 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:043df9f67e9a9e13698b6da176cf64025a7983a5f0cb5b4c0b7659a9f3e7c288`  
		Last Modified: Wed, 19 Jan 2022 22:08:36 GMT  
		Size: 99.1 MB (99103465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
