## `eclipse-temurin:8-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:6a88c60ed4adc4e7bc5e2729fe76a83b4a45e02bd6cf7967f26f1344f197bde3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:27a0b5488c1a4ef3d352ee07fd0ca2c8179de882ad27fea2e0fc907f68b8dbb8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **113.4 MB (113386116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4ce2440f7845d58b08e21af6b3bcd7acaf4cf008add4656b00db90dc9ce1ced`
-	Entrypoint: `["\/entrypoint.sh"]`

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
# Tue, 08 Aug 2023 19:19:46 GMT
RUN apk add --no-cache fontconfig java-cacerts libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Tue, 08 Aug 2023 19:19:46 GMT
ENV JAVA_VERSION=jdk8u382-b05
# Tue, 08 Aug 2023 19:19:52 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='6cf2d4925c387c4cdc0bf2e71de3690527141b5244695d0b3109ce83a8512235';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 08 Aug 2023 19:19:53 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Tue, 08 Aug 2023 19:19:53 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:19:53 GMT
ENTRYPOINT ["/entrypoint.sh"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8fb73fc61a1a25f2a3dc05916ccac6537b166b6bb8aec0290fccb908e4e46e9`  
		Last Modified: Tue, 08 Aug 2023 19:26:28 GMT  
		Size: 8.5 MB (8495235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2787d95686926435132bae64a14bec1de94e99ece5b089a41b1505b76578f78`  
		Last Modified: Tue, 08 Aug 2023 19:26:33 GMT  
		Size: 101.5 MB (101488443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf529086b40e1d7b309405b23a5493a0961a0cf7d01f88fc9469b968b781465e`  
		Last Modified: Tue, 08 Aug 2023 19:26:24 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72312418e41046079c168dcc7308206d6e331d847000f58f9c751f8e08fca152`  
		Last Modified: Tue, 08 Aug 2023 19:26:24 GMT  
		Size: 665.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
