## `eclipse-temurin:11-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:640394e78d775da90fa63a04c56f5b2d024455ff67d8799fb62bf097e5694a60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:11-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ba4a5510ef45a98ed37838b0db2a82e05016b9950a7c9a3ddcc5c4adde5a538b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (45951148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e8f2ec64e08366c275633e1740fdbc897e77d523f2dda938d47b7732c037424`
-	Default Command: `["\/bin\/sh"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 08:42:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Mar 2022 08:42:17 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Thu, 17 Mar 2022 08:42:49 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Thu, 17 Mar 2022 08:43:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6af0a3a37d4d6ca2b7f542184b47560339635c382f5ba13a9baf1c140671a826';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jre_x64_alpine-linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Mar 2022 08:43:16 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 08:43:16 GMT
RUN echo Verifying install ...     && echo java --version && java --version     && echo Complete.
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d724c850e02b04db420d6d1310332dafdcbf4f8f4280d76ed66954a1b5d0f4d`  
		Last Modified: Thu, 17 Mar 2022 08:46:33 GMT  
		Size: 430.3 KB (430324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b96e997e4f624d9d1e0f3fdfaf5cd300c982343415e73494aeb3426afbb55c4d`  
		Last Modified: Thu, 17 Mar 2022 08:47:52 GMT  
		Size: 42.7 MB (42708028 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c65f8bd9601b62084598e0a5425a86762bdba5c6dce05282f80a622b1942783`  
		Last Modified: Thu, 17 Mar 2022 08:47:44 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
