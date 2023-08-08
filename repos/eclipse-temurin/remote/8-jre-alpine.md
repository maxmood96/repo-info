## `eclipse-temurin:8-jre-alpine`

```console
$ docker pull eclipse-temurin@sha256:3c3c911820104a05770f6ad9c1667bc42e4b037f1d6740c603330dc6ddaa2364
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:8-jre-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:ecf9117c9343560bda6056cfa1210fdd856c55e5af3f4ef759cad58536a91cb1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53688175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c346e933cd6a3607ef4070f3db2e126c94af8c7a7ee6d193046db37e5eb8b785`
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
# Tue, 08 Aug 2023 19:21:20 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='7040d865493f13204194c5a1add63e22516b1fa4481264baa6a5b2614a275a0e';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u382-b05/OpenJDK8U-jre_x64_alpine-linux_hotspot_8u382b05.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 08 Aug 2023 19:21:21 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 08 Aug 2023 19:21:21 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:21:21 GMT
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
	-	`sha256:e37946a2ce341c49af2fe78bfd7b44663e7d24724239195418c5e5fa36e80016`  
		Last Modified: Tue, 08 Aug 2023 19:27:52 GMT  
		Size: 41.8 MB (41790501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe02948490d7dc6e35dfc3ed7ee921a74c872193ffcab75e2e357baa2ce42b7`  
		Last Modified: Tue, 08 Aug 2023 19:27:47 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223b53628ce21175ff54e3136aeba82f786455e4925712d3b6daddee06cff411`  
		Last Modified: Tue, 08 Aug 2023 19:27:47 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
