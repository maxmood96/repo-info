## `eclipse-temurin:17-alpine`

```console
$ docker pull eclipse-temurin@sha256:654d5f241f646e1314a1042343acc7d0247449421038489c3aca62576e2911e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:17-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:33d37361a987f77f6cca0b334dba2c543d59387fff8a4d7f5490b6344a7c0888
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **156.0 MB (156002644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c077a2ae9a37c3ce730ab4b9c3f3417dadc124e559ab50ad52ce5123379d9928`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["jshell"]`

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
# Tue, 08 Aug 2023 19:23:02 GMT
ENV JAVA_VERSION=jdk-17.0.8+7
# Tue, 08 Aug 2023 19:23:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='90eb413eeed9cc2813f7d66d348c35475148c0cdc41c8f9ef2f26d51078e287e';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.8%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.8_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Tue, 08 Aug 2023 19:23:14 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 08 Aug 2023 19:23:14 GMT
COPY file:0673fe0a4a716089bcd96321c8de60149aea8a94ae7c4ba827ecc4a74a9789a3 in / 
# Tue, 08 Aug 2023 19:23:14 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 08 Aug 2023 19:23:15 GMT
CMD ["jshell"]
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
	-	`sha256:b08bd1ee4ee86d676d18881ed53eb9a95f4983e81bc1610c8d0cf85655c12370`  
		Last Modified: Tue, 08 Aug 2023 19:31:29 GMT  
		Size: 144.1 MB (144104954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc47667d039ce2232e2793527753e82ad1e8094973f649c93dfd495b95e2096a`  
		Last Modified: Tue, 08 Aug 2023 19:31:16 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ce924bc6305f60da9e897c1cd150884130e50c9f5d9874cb58fb5527ab8dfb`  
		Last Modified: Tue, 08 Aug 2023 19:31:16 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
