## `eclipse-temurin:8-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:8a8fbfd1e27b904cefa06d369773aadb6d8952bebeb4e9750f8b46b9e0e966a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:f488be2688fba9d90554802b57a45c93c7d550e884c1006fc8d3e098276ca69f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **114.2 MB (114167522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4c7591aba6dd4fbbab8ce5f8f55a29746a77af0b68c564787786068378f09b`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 19:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Aug 2023 19:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 19:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Aug 2023 18:09:08 GMT
RUN apk add --no-cache fontconfig java-cacerts bash libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 14 Aug 2023 18:09:08 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Mon, 14 Aug 2023 18:09:15 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6cf2d4925c387c4cdc0bf2e71de3690527141b5244695d0b3109ce83a8512235';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Mon, 14 Aug 2023 18:09:16 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Mon, 14 Aug 2023 18:09:16 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:16 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994e83f716a0db024fb37caf707eae5af27172a0fffb691c6e7b53bb7fc5b3ab`  
		Last Modified: Mon, 14 Aug 2023 18:13:07 GMT  
		Size: 9.3 MB (9276497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3718ddfde565169ebbf58b9bc0c6501e01ca1f6000dffc7a63c6902d293cdc63`  
		Last Modified: Mon, 14 Aug 2023 18:13:14 GMT  
		Size: 101.5 MB (101488519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68cf8eb84665661db22fccb75e00df2629560ad1c0cbbcf163df0bef4ee90c9e`  
		Last Modified: Mon, 14 Aug 2023 18:13:05 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aea6da927b0cd89ba488aa730b537cab0539b16c96eee6b8eb2a50f712761bfd`  
		Last Modified: Mon, 14 Aug 2023 18:12:17 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
