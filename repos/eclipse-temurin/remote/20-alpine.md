## `eclipse-temurin:20-alpine`

```console
$ docker pull eclipse-temurin@sha256:38e00a5fcb2a337897387f40f2b6603522d1917bae565be565909ffd6b7f48c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:20-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:7ebbe07fff751864f213e0d5a00948c118165b830e5bebc4f5cd793449dc2711
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165610235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48ffb0cc2f17c760c186eb7ae85ae535d7781f4c92d1f8154dcbd1de6fe7dbed`
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
# Thu, 28 Sep 2023 23:26:28 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Thu, 28 Sep 2023 23:26:39 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b03aced4b7a1c49bc00297e35e45480fd03818862b93e17e1551a3b721e89306';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_alpine-linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 28 Sep 2023 23:26:41 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 28 Sep 2023 23:26:41 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 28 Sep 2023 23:26:41 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 28 Sep 2023 23:26:41 GMT
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
	-	`sha256:2d4780bd88e540ffc3aff06007363d67ee5849f55861ee9c03d071f8878b194e`  
		Last Modified: Thu, 28 Sep 2023 23:30:46 GMT  
		Size: 152.9 MB (152930846 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd951bcdd02682030bc58f966174743a3cab42dee968ef682f2166c1f4215de7`  
		Last Modified: Thu, 28 Sep 2023 23:30:31 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e76b0f81ae3a0cca78c8906b0bea646fac04c6b7abfcf3349bca0fb3532c2975`  
		Last Modified: Thu, 28 Sep 2023 23:30:31 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
