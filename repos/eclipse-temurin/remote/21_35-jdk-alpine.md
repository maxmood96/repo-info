## `eclipse-temurin:21_35-jdk-alpine`

```console
$ docker pull eclipse-temurin@sha256:0590276e28eadad32040b43c6564a991a3860049155be0c69e7d3632ead05f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `eclipse-temurin:21_35-jdk-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:86a08690ee24ed6c6723d8abf74aee2078faa511f69802b327792f2188d46450
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **170.3 MB (170309441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9012db75c0af5883cd07a1c8ff1fc391e90d7e08cfd8cfd7393776d3ae123aee`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Wed, 11 Oct 2023 18:09:20 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 18:09:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3f8e5b0447d2dd711f12edda611ed1cf9aab4ca53c8fe32fca8fb1e6fee41c12';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21_35.tar.gz';          ;;        amd64|x86_64)          ESUM='4fd74f93f0b1a94d8471e0ed801fe9d938f7471f6efe8791880c85e7716c943f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 11 Oct 2023 18:09:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Oct 2023 18:09:33 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 11 Oct 2023 18:09:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Oct 2023 18:09:33 GMT
CMD ["jshell"]
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
	-	`sha256:aa15de4e91b4ea2bb2143d98dec470476fe69008037a626991da945af66ff8b9`  
		Last Modified: Wed, 11 Oct 2023 18:12:45 GMT  
		Size: 157.6 MB (157630049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57006341305b6b066a0078ba7cc1b938820d7008118025c4873bfd0efac05c23`  
		Last Modified: Wed, 11 Oct 2023 18:12:32 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a0f8d9e2d3f3ae2db5bd1c8a0c85b7b197dc7ab45c6a2797eebc228fe69a3f`  
		Last Modified: Wed, 11 Oct 2023 18:12:32 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `eclipse-temurin:21_35-jdk-alpine` - linux; arm64 variant v8

```console
$ docker pull eclipse-temurin@sha256:0ee18c1da1ab7a8f1adf29a1583d843ce594d31eddb3d5c79e50145d78a262f4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **168.4 MB (168410075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bbe55f77af91a511eca783231647e77c556e7b04fc85dd17303b4177a0e2ea8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Wed, 11 Oct 2023 17:34:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 11 Oct 2023 17:34:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 Oct 2023 17:34:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 11 Oct 2023 17:34:07 GMT
RUN apk add --no-cache fontconfig java-cacerts bash libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 11 Oct 2023 17:34:07 GMT
ENV JAVA_VERSION=jdk-21+35
# Wed, 11 Oct 2023 17:34:17 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3f8e5b0447d2dd711f12edda611ed1cf9aab4ca53c8fe32fca8fb1e6fee41c12';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21_35.tar.gz';          ;;        amd64|x86_64)          ESUM='4fd74f93f0b1a94d8471e0ed801fe9d938f7471f6efe8791880c85e7716c943f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 11 Oct 2023 17:34:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 11 Oct 2023 17:34:20 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Wed, 11 Oct 2023 17:34:20 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 11 Oct 2023 17:34:20 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2228a2df1abfbeae54864f3e7bdf8cf1b470db721a527c93efbae0c95f784d`  
		Last Modified: Wed, 11 Oct 2023 17:36:52 GMT  
		Size: 9.4 MB (9435446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4983f820c3ffd082e7c998b0460911fbb7b82a0c849ae61be2d6e79a94297da9`  
		Last Modified: Wed, 11 Oct 2023 17:37:04 GMT  
		Size: 155.6 MB (155641888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:929ff439665ce1216e8375084511e48a61629ead81890681c1eebf935b80dd26`  
		Last Modified: Wed, 11 Oct 2023 17:36:51 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5b699de1caa2c0044963756ab749d3923c6b5b712f8e1753821d78b9efece9`  
		Last Modified: Wed, 11 Oct 2023 17:36:51 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
