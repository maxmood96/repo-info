## `amazoncorretto:11-alpine3.17-jdk`

```console
$ docker pull amazoncorretto@sha256:3c740c1747de7c36ff66e6989978e2bbade7ca24e6f6008585a2842a81909aa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `amazoncorretto:11-alpine3.17-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:7bffa2b1c96266faadf80087d1837e0e8be339e4d7ce104e541068486e4a4c98
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **198.6 MB (198558216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be19c490f51fbfd4d3bfcf9e77956cd0e455f5933fe4b64164f3ee34e6fcde1c`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 18:23:17 GMT
ARG version=11.0.19.7.1
# Thu, 20 Apr 2023 18:23:24 GMT
# ARGS: version=11.0.19.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 20 Apr 2023 18:23:25 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 18:23:25 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 18:23:25 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad8dd74d3cfe97ed1fd9b2db3bb14d353c4bd304be589987a262aecd64012c82`  
		Last Modified: Thu, 20 Apr 2023 18:33:59 GMT  
		Size: 195.2 MB (195183653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `amazoncorretto:11-alpine3.17-jdk` - linux; arm64 variant v8

```console
$ docker pull amazoncorretto@sha256:2b9c299376427fe2823d420f914a08373f3ab5a3d2ce934ec86bc92223b3596d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196731327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7433e76f81673294a9ad7e4b19f602886504c1574261d1ba13b607455e8dce51`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:18 GMT
ADD file:e51d4089e73ad6dee52b31f0c8059a00c17df6e23f6741fe11b43bd84cc99008 in / 
# Wed, 29 Mar 2023 17:39:18 GMT
CMD ["/bin/sh"]
# Thu, 20 Apr 2023 17:42:37 GMT
ARG version=11.0.19.7.1
# Thu, 20 Apr 2023 17:42:42 GMT
# ARGS: version=11.0.19.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-11=$version-r0
# Thu, 20 Apr 2023 17:42:44 GMT
ENV LANG=C.UTF-8
# Thu, 20 Apr 2023 17:42:44 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Thu, 20 Apr 2023 17:42:44 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:c41833b44d910632b415cd89a9cdaa4d62c9725dc56c99a7ddadafd6719960f9`  
		Last Modified: Wed, 29 Mar 2023 17:39:44 GMT  
		Size: 3.3 MB (3261854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bbf01842844b2d558642c3326b72f93b7c5bac19551e279343f3043710a8cd0`  
		Last Modified: Thu, 20 Apr 2023 17:52:44 GMT  
		Size: 193.5 MB (193469473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
