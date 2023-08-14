## `eclipse-temurin:20-alpine`

```console
$ docker pull eclipse-temurin@sha256:7a5943383c29fd3ce1d5f60bf70adaa2b3b0f6fa8364cf47c2065e1f26eef236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `eclipse-temurin:20-alpine` - linux; amd64

```console
$ docker pull eclipse-temurin@sha256:27f64fb39e4e052bba5fdd4659875b8ab421eb3c5d85ab9d4a8025808fc39cfa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **165.6 MB (165609861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:994ee3e5cefc65e041647f32af953fffa56484bd1758bd67fa2dea0e9f6618c5`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
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
# Mon, 14 Aug 2023 18:09:08 GMT
RUN apk add --no-cache fontconfig java-cacerts bash libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 14 Aug 2023 18:11:21 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Mon, 14 Aug 2023 18:11:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b03aced4b7a1c49bc00297e35e45480fd03818862b93e17e1551a3b721e89306';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_alpine-linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Mon, 14 Aug 2023 18:11:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:11:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:11:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 18:11:35 GMT
CMD ["jshell"]
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
	-	`sha256:b4f448552bb15ae7982f30b7bf23aac44717ed6365a7a879d53de4c79d78622d`  
		Last Modified: Mon, 14 Aug 2023 18:18:33 GMT  
		Size: 152.9 MB (152930841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bdfae8054477c91597828697217510a2f61d4c33e790ad929e88b8d9903e2a`  
		Last Modified: Mon, 14 Aug 2023 18:18:21 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7f96622c1da1429f1ec4655cd421ba42bf1bfc9532f6eb6d5f12679b6eb955`  
		Last Modified: Mon, 14 Aug 2023 18:18:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
