## `eclipse-temurin:19-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:fabe27bd9db502d484a11d3f571c2f4ef7bba4a172527084d939935358fb06c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:19-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:a75ea64f676041562cd7d3a54a9764bbfb357b2bf1bebf46e2af73e62d32e36c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.5 MB (64529052 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f10fe2918b92d0aa69fc06c5f77b81ccdba3e188b047524031e4cb20d602cba7`
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
# Mon, 09 Jan 2023 17:42:15 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Mon, 09 Jan 2023 17:42:50 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='32426b790ac99a21a69abec793bfa47996a4fe7f74c7c89484836237f121640b';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jre_x64_alpine-linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Mon, 09 Jan 2023 17:42:51 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
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
	-	`sha256:a8cf960fcec52565486b0993f2f077c7cffdb436a39203d7e5eaa86d76100240`  
		Last Modified: Mon, 09 Jan 2023 17:47:31 GMT  
		Size: 49.1 MB (49138130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a6b95e438483873516c83dc94ee69d3c89fcd42b797ad18464ed512fefca8e`  
		Last Modified: Mon, 09 Jan 2023 17:47:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
