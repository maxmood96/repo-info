## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:9499fad4ceb7a163d7d7eaab4b21c6151b2827c2ad2f4104a95fcdafd6422c44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:4f27a2ba26e0d34478cdd9f51f77692d7e80ff60426d907e3d59e909e61beb9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **167.6 MB (167555268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa087c55682abbd407f5ad8827d737e81fa0beb9d88ae8614f7694271734e93f`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 20 Aug 2024 18:12:59 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["/bin/sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 20 Aug 2024 18:12:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 20 Aug 2024 18:12:59 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENV JAVA_VERSION=jdk-11.0.24+8
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        x86_64)          ESUM='ae988c72eeb2d78bb729a3387601ce0ea84305734ebdbe95d276f39952a8e019';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.24%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.24_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["jshell"]
# Tue, 20 Aug 2024 18:12:59 GMT
RUN apk add --no-cache bash procps curl tar openssh-client # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.title=Apache Maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.source=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.url=https://github.com/carlossg/docker-maven
# Tue, 20 Aug 2024 18:12:59 GMT
LABEL org.opencontainers.image.description=Apache Maven is a software project management and comprehension tool. Based on the concept of a project object model (POM), Maven can manage a project's build, reporting and documentation from a central piece of information.
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven /usr/share/maven # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/local/bin/mvn-entrypoint.sh /usr/local/bin/mvn-entrypoint.sh # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
COPY /usr/share/maven/ref/settings-docker.xml /usr/share/maven/ref/settings-docker.xml # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
RUN ln -s ${MAVEN_HOME}/bin/mvn /usr/bin/mvn # buildkit
# Tue, 20 Aug 2024 18:12:59 GMT
ARG MAVEN_VERSION=3.9.9
# Tue, 20 Aug 2024 18:12:59 GMT
ARG USER_HOME_DIR=/root
# Tue, 20 Aug 2024 18:12:59 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 20 Aug 2024 18:12:59 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 20 Aug 2024 18:12:59 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae396f4785e0f5ffe9faa9dba4e1459ed98a5ff838938e30aee734ec99a9b51`  
		Last Modified: Sat, 19 Oct 2024 00:55:14 GMT  
		Size: 9.4 MB (9389044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d163b41500a9f32eecafcf15f19f5bf9a470e46c97ec782a09649b5ed4cbf60`  
		Last Modified: Sat, 19 Oct 2024 00:55:19 GMT  
		Size: 140.7 MB (140723916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:793f85645d0cce61f3975ee335a1c386af87645ef97849cef077ccd6b22c877f`  
		Last Modified: Sat, 19 Oct 2024 00:55:14 GMT  
		Size: 129.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92f0a6d5c7b7b83e0f12f11eca18914175b571bd4fc537ed13c2af26037c4c3c`  
		Last Modified: Sat, 19 Oct 2024 00:55:14 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12b83f1638105b9924649a5674df905a2cc022442a6aa52802b24c2adafd4d0d`  
		Last Modified: Sat, 19 Oct 2024 03:58:20 GMT  
		Size: 4.6 MB (4644779 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb49ea604af5d34b0db5d87540df847f39f77e07105b38de28f3f7ac61eeb8d9`  
		Last Modified: Sat, 19 Oct 2024 03:58:20 GMT  
		Size: 9.2 MB (9170443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4a9289214f8113f7e48a99c451906677132db3dffcc4ae63fe767aa9ce0ea7`  
		Last Modified: Sat, 19 Oct 2024 03:58:19 GMT  
		Size: 858.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90899a0c8833ad0beb57c8fa4c95dbe11058e81c224dff11622ad35e70813039`  
		Last Modified: Sat, 19 Oct 2024 03:58:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `maven:3-eclipse-temurin-11-alpine` - unknown; unknown

```console
$ docker pull maven@sha256:ef0dd2e1803809d30a7b1a76ffe9512cfb006ba0e49804999c906de00a5ee82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1074362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66673104632b01f84676dc2a605c12885240c2286399cfd3b9e50aed701b2827`

```dockerfile
```

-	Layers:
	-	`sha256:7fd9d6fb6e15ed0771a460d4ad6c7f5f8262d494401e17855254c12ebe740761`  
		Last Modified: Sat, 19 Oct 2024 03:58:19 GMT  
		Size: 1.1 MB (1054985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3bf34cff12576e30a624b2a8ba9b2d3d5cf9d0782398ad64bd9015d52024c1c8`  
		Last Modified: Sat, 19 Oct 2024 03:58:19 GMT  
		Size: 19.4 KB (19377 bytes)  
		MIME: application/vnd.in-toto+json
