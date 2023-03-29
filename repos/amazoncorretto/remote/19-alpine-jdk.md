## `amazoncorretto:19-alpine-jdk`

```console
$ docker pull amazoncorretto@sha256:21cc27d3f3a4a79b32c060bd55576a22922a2a70bfe7a6b3a886ad8119ecc174
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `amazoncorretto:19-alpine-jdk` - linux; amd64

```console
$ docker pull amazoncorretto@sha256:cd7b4a7e3daf05961375138c3cfbe91d14028842f544bad04e40fdebeaf05db3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **205.5 MB (205461927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b700372727f499e23d2f2258756e1aa3ca60116f738722e3294d15aa721a886`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:24 GMT
ADD file:9a4f77dfaba7fd2aa78186e4ef0e7486ad55101cefc1fabbc1b385601bb38920 in / 
# Wed, 29 Mar 2023 18:19:24 GMT
CMD ["/bin/sh"]
# Wed, 29 Mar 2023 19:19:38 GMT
ARG version=19.0.2.7.1
# Wed, 29 Mar 2023 19:19:45 GMT
# ARGS: version=19.0.2.7.1
RUN wget -O /THIRD-PARTY-LICENSES-20200824.tar.gz https://corretto.aws/downloads/resources/licenses/alpine/THIRD-PARTY-LICENSES-20200824.tar.gz &&     echo "82f3e50e71b2aee21321b2b33de372feed5befad6ef2196ddec92311bc09becb  /THIRD-PARTY-LICENSES-20200824.tar.gz" | sha256sum -c - &&     tar x -ovzf THIRD-PARTY-LICENSES-20200824.tar.gz &&     rm -rf THIRD-PARTY-LICENSES-20200824.tar.gz &&     wget -O /etc/apk/keys/amazoncorretto.rsa.pub https://apk.corretto.aws/amazoncorretto.rsa.pub &&     SHA_SUM="6cfdf08be09f32ca298e2d5bd4a359ee2b275765c09b56d514624bf831eafb91" &&     echo "${SHA_SUM}  /etc/apk/keys/amazoncorretto.rsa.pub" | sha256sum -c - &&     echo "https://apk.corretto.aws" >> /etc/apk/repositories &&     apk add --no-cache amazon-corretto-19=$version-r0
# Wed, 29 Mar 2023 19:19:45 GMT
ENV LANG=C.UTF-8
# Wed, 29 Mar 2023 19:19:45 GMT
ENV JAVA_HOME=/usr/lib/jvm/default-jvm
# Wed, 29 Mar 2023 19:19:45 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/lib/jvm/default-jvm/bin
```

-	Layers:
	-	`sha256:f56be85fc22e46face30e2c3de3f7fe7c15f8fd7c4e5add29d7f64b87abdaa09`  
		Last Modified: Wed, 29 Mar 2023 18:19:57 GMT  
		Size: 3.4 MB (3374563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51109911178b6fbeede1da8166e599f68f822dc0bf185cff7c80f4881bc3ec81`  
		Last Modified: Wed, 29 Mar 2023 19:29:10 GMT  
		Size: 202.1 MB (202087364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
