## `eclipse-temurin:20-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:29928dae72de0d8b6351b77726357f0e44d1f97908c23192cdcf501147d42601
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:20-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:987af6a7e762cf950598c8f5ebaad9fff9dcf220fc8a3bddb9fd55b49b48a3e4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62642630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee85abd283e241f811f01d10473121bd56a5450141ac9d4f33b38072b88509c8`
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
# Mon, 14 Aug 2023 18:11:21 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Mon, 14 Aug 2023 18:11:48 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='53b34747a3c042a4cccb2b8b78fba3330b105bc523f0861237baa9143dc39115';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jre_x64_alpine-linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Mon, 14 Aug 2023 18:11:49 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:11:49 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:11:49 GMT
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
	-	`sha256:34f3145f835e459f7f8841a7801e3632e9f4728de845078f8d43843284a96671`  
		Last Modified: Mon, 14 Aug 2023 18:19:09 GMT  
		Size: 50.0 MB (49963625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbbbde20516d18a82083ebf3c579428527bc41b4e30a1a0060aae8d63e00c06f`  
		Last Modified: Mon, 14 Aug 2023 18:19:02 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf4cb78d729d069d1b9d0478ca1fc6b768f2defd48b2b860b33ac4cdc9105b5`  
		Last Modified: Mon, 14 Aug 2023 18:19:02 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
