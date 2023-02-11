## `amazoncorretto:8-alpine3.14`

```console
$ docker pull amazoncorretto@sha256:b1702bd53799958914a7490a05e5206a26f8d64d47471577fc0fbf2e276818f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:8-alpine3.14` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:9870560d951696c29a53edf604feeb0df12e2bf96de005fd17933d5d5027a90d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **102.9 MB (102861474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9f79e0abeffaf504e6ae32f9d2ca60c818699438ace94eea692aff597de7ec1`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:59 GMT
ADD file:a41bb436701fd0adf99a3157d19f172b3e54ea033f5c617009e2d1bdeac206d7 in / 
# Sat, 11 Feb 2023 04:46:59 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 06:58:30 GMT
ARG version=8.362.08.1
# Sat, 11 Feb 2023 06:58:37 GMT
# ARGS: version=8.362.08.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-8=$version-r0
# Sat, 11 Feb 2023 06:58:37 GMT
ENV LANG=C.UTF-8
# Sat, 11 Feb 2023 06:58:37 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Sat, 11 Feb 2023 06:58:37 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:d261077062b2aebb9ca8dc61f2b00e7e2b4e44179d3cfbe526c4ee0c5e41b26f`  
		Last Modified: Sat, 11 Feb 2023 04:47:49 GMT  
		Size: 2.8 MB (2829633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc22219d1ff7b9c60a9dc81474032deb4f92ec4e6f995a1f61f61c0c6a4dcb1`  
		Last Modified: Sat, 11 Feb 2023 07:03:50 GMT  
		Size: 100.0 MB (100031841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
