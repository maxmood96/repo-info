## `amazoncorretto:8u342-alpine3.16-jre`

```console
$ docker pull amazoncorretto@sha256:c6134368477801265f2012adfa39a0d94d0de62c3b0feef8d94d7451f36d71d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8u342-alpine3.16-jre` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:d8d0475c7c8e6b0a12c79755c66d6ff3fa8e0a236295119981d9e00e2ba44947
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43245414 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6e92f7c570b4f244fbf90fcfbd5d4a361f6da051f76e314847ce5454c28a9769`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 28 Sep 2022 21:19:45 GMT
ARG version=8.342.07.4
# Wed, 28 Sep 2022 21:19:56 GMT
# ARGS: version=8.342.07.4
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8-jre=$version-r0
# Wed, 28 Sep 2022 21:19:56 GMT
ENV LANG=C.UTF-8
# Wed, 28 Sep 2022 21:19:56 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm/jre
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e364bec0c5e96af9dc33b3ed9c77c70615ba6cd4d80ed20fa991165eed742b38`  
		Last Modified: Wed, 28 Sep 2022 21:24:02 GMT  
		Size: 40.4 MB (40439360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
