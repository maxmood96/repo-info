## `amazoncorretto:8u362-alpine3.16`

```console
$ docker pull amazoncorretto@sha256:7813572de53dc73a8d66a1ef0dd77675072c8f3acb0c3432005e289f73262962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u362-alpine3.16` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:33dcf44564b3773ebbdaf782a5586dea89cda3bb643b6d89722a1fc5cee69fb9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.8 MB (102839698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7362a7ce86ff439f86affdd7957466c74c31a70ae9e716b60e63e6e2ea0248a`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:50 GMT
ADD file:ac5fb7eb0d68040d948989f0a50914d0d4a6b631cfe76b508eecd82eb7d46953 in / 
# Sat, 11 Feb 2023 04:46:50 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:58:57 GMT
ARG version=8.362.08.1
# Sat, 11 Feb 2023 06:59:01 GMT
# ARGS: version=8.362.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Sat, 11 Feb 2023 06:59:01 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 06:59:02 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 11 Feb 2023 06:59:02 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:ef5531b6e74e7865f5d142926b572d742ad47c153211de707903b4f5dd8d9e77`  
		Last Modified: Sat, 11 Feb 2023 04:47:32 GMT  
		Size: 2.8 MB (2807762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94625df41bc981397615ec1ec3033a44478c2b5dca0266e4c858a2d846e4b78e`  
		Last Modified: Sat, 11 Feb 2023 07:05:00 GMT  
		Size: 100.0 MB (100031936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
