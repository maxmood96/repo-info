## `eclipse-temurin:8-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:2ba67f00ca07c8fe03b08ddf3255cd9c5cc10da3865a90d72bbbb8bbda3bd29a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:b4659e359fccdbd9e03ccd9259052c4c5fe39d6cddf01d95fdd9ee9505815919
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114167830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d56a79d3f68b0a304d4abdf7d430c186a1199a78cc14d14299c28eae7bc188d1`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 28 Sep 2023 23:24:23 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 28 Sep 2023 23:24:23 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 28 Sep 2023 23:24:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 28 Sep 2023 23:24:25 GMT
RUN apk add --no-cache fontconfig java-cacerts bash libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 28 Sep 2023 23:24:26 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Thu, 28 Sep 2023 23:24:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6cf2d4925c387c4cdc0bf2e71de3690527141b5244695d0b3109ce83a8512235';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 28 Sep 2023 23:24:32 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 28 Sep 2023 23:24:33 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 28 Sep 2023 23:24:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34e4092d737c5d0c601ddadd8d075b756e55cc717065ae83683571965c2117a9`  
		Last Modified: Thu, 28 Sep 2023 23:28:20 GMT  
		Size: 9.3 MB (9276514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1076f6323c43e5087d2bb95d374dc7a408505995c17d3f38e5ddf3aa8774487`  
		Last Modified: Thu, 28 Sep 2023 23:28:28 GMT  
		Size: 101.5 MB (101488457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7530e3dbc8ddd8a31ebcf9a552cfee323caa314e496b064c11f5396d5bd9f80b`  
		Last Modified: Thu, 28 Sep 2023 23:28:19 GMT  
		Size: 159.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05429726b5869b70315ac86c634ec1babe60b99b3bad24c2e55a622663f586ac`  
		Last Modified: Thu, 28 Sep 2023 23:28:19 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
