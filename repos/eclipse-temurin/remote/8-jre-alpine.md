## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:27c678c54bf141c4fd201de63c86b62dc4713e7a7a215f5e0b96e5e735abde3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:5397c9a98650c37a52d2c79207a45383a0886c90b49445f39b73f3efee9668d8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.2 MB (57159014 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59a6b034652053201bc9d637ac12cefe65ab3048584d2e4866a3be74a94bbc86`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:40:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Jan 2023 17:40:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 17:40:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Jan 2023 17:40:11 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 09 Jan 2023 17:40:11 GMT
ENV JAVA_VERSION=jdk8u352-b08
# Mon, 09 Jan 2023 17:40:34 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='0f4a4a3c092d8cca171fc36003ac82e2f3d8d768bd6f530a20e2a4caf79bdb9e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u352-b08/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u352b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Mon, 09 Jan 2023 17:40:35 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e3b32ee5a149e3ccb99051cdb52e96e11488293cdf72ee88168c88dd335c7`  
		Last Modified: Mon, 09 Jan 2023 17:44:40 GMT  
		Size: 12.0 MB (12020134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9016bbb79adbedb65d58f59d9d150a07994632fb60d9b87a607175be3580052`  
		Last Modified: Mon, 09 Jan 2023 17:45:07 GMT  
		Size: 41.8 MB (41768092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1cb99de928bea1fd694c4ae2c44607db0553b2673803a1b27bc9fa34b598eb2`  
		Last Modified: Mon, 09 Jan 2023 17:45:02 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
