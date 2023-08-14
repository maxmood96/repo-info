## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:6861e72db8f1bf23b71f3ad100f173d7260439675944e11b2a59cb30c6640e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:e586cd2d4d26073164aefe90ad88ab632b548d850aac384fb70dfdf42ff58968
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54469543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7a454a165aee94679b56c6850bb231d3dfbfb021398e99aad775d898ff766d8`
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
# Mon, 14 Aug 2023 18:09:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7040d865493f13204194c5a1add63e22516b1fa4481264baa6a5b2614a275a0e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Mon, 14 Aug 2023 18:09:34 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Mon, 14 Aug 2023 18:09:34 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:09:34 GMT
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
	-	`sha256:0fd9b0bc205af3b8c416ed85a948c6a2e9fba074669a240f7ffa1300adead8c4`  
		Last Modified: Mon, 14 Aug 2023 18:14:08 GMT  
		Size: 41.8 MB (41790537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d78ed189eaa2e9ae439d524ef2e11b0aebe3001ee9949355bdef36ca078f26f3`  
		Last Modified: Mon, 14 Aug 2023 18:14:03 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8c0d4a1159cc19d67888c8291165de0f40ca5f2a78426a480b54c93cef46af`  
		Last Modified: Mon, 14 Aug 2023 18:13:45 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
