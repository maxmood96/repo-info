## `maven:3-eclipse-temurin-8-alpine`

```console
$ docker pull maven@sha256:3183294048db1398f38205b4d9e6a6cd4b006b5ec398c3acb70c76ed03a2965a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-8-alpine` - linux; amd64

```console
$ docker pull maven@sha256:ac88d584f6455059e11ff7beb2c17bc401396bfba9a66fdc434432f4eed5a51b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.4 MB (78434219 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c72937078ef83e854c9b8475ba4bc5668b2ccd4a3df91a59113e353da09d68e5`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Sat, 11 Feb 2023 04:46:42 GMT
ADD file:40887ab7c06977737e63c215c9bd297c0c74de8d12d16ebdf1c3d40ac392f62d in / 
# Sat, 11 Feb 2023 04:46:42 GMT
CMD ["/bin/sh"]
# Sat, 11 Feb 2023 05:24:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 11 Feb 2023 05:24:07 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Feb 2023 05:24:07 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 11 Feb 2023 05:24:09 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Sat, 11 Feb 2023 05:24:09 GMT
ENV JAVA_VERSION=jdk8u362-b09
# Sat, 11 Feb 2023 05:24:18 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='389c0d2ea59742103f46f1dd6d2c83e43e9f935f3f0485b1f9e74ac4e8c5ce47';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u362-b09/OpenJDK8U-jdk_x64_alpine-linux_hotspot_8u362b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;
# Sat, 11 Feb 2023 05:24:19 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 11 Feb 2023 06:06:23 GMT
RUN apk add --no-cache curl tar bash procps
# Sat, 11 Feb 2023 06:06:24 GMT
ARG MAVEN_VERSION=3.8.7
# Sat, 11 Feb 2023 06:06:24 GMT
ARG USER_HOME_DIR=/root
# Sat, 11 Feb 2023 06:06:24 GMT
ARG SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27
# Sat, 11 Feb 2023 06:06:24 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries
# Sat, 11 Feb 2023 06:06:25 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.7/binaries MAVEN_VERSION=3.8.7 SHA=21c2be0a180a326353e8f6d12289f74bc7cd53080305f05358936f3a1b6dd4d91203f4cc799e81761cf5c53c5bbe9dcc13bdb27ec8f57ecf21b2f9ceec3c8d27 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Sat, 11 Feb 2023 06:06:26 GMT
ENV MAVEN_HOME=/usr/share/maven
# Sat, 11 Feb 2023 06:06:26 GMT
ENV MAVEN_CONFIG=/root/.m2
# Sat, 11 Feb 2023 06:06:26 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Sat, 11 Feb 2023 06:06:26 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Sat, 11 Feb 2023 06:06:26 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Sat, 11 Feb 2023 06:06:26 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:63b65145d645c1250c391b2d16ebe53b3747c295ca8ba2fcb6b0cf064a4dc21c`  
		Last Modified: Fri, 10 Feb 2023 22:41:31 GMT  
		Size: 3.4 MB (3374446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f55337210c571172bc884a7dfb6dc597adab6b6ef741c06ca3200884ffc4b2b`  
		Last Modified: Sat, 11 Feb 2023 05:28:55 GMT  
		Size: 12.0 MB (12020168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a9a27ee80bf5356fe3adbe48eac6901f6ce624403650042a5c0821c6dc9f552`  
		Last Modified: Sat, 11 Feb 2023 05:29:00 GMT  
		Size: 52.5 MB (52541360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9025552edcd6ac4129d2174472698d2c715f51edd32706646362a8c24bda200`  
		Last Modified: Sat, 11 Feb 2023 05:28:54 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d58e7d2bd374df586ab75ffab508c330c07f4a58c921dda0d9ac50ac5afb1f5`  
		Last Modified: Sat, 11 Feb 2023 06:08:40 GMT  
		Size: 2.1 MB (2145733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86ecde8478337d79d6228af7bd2db23fd4fb599828beba464e13a51c52d2e3bb`  
		Last Modified: Sat, 11 Feb 2023 06:08:41 GMT  
		Size: 8.4 MB (8351138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4135a7019201abcfe50e22f54e2ae5116c0aa1294d75a17339d925886554819d`  
		Last Modified: Sat, 11 Feb 2023 06:08:40 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8869195ec03aac4927c97c795e29f149e30241723a3b94d280b88d49782c44f`  
		Last Modified: Sat, 11 Feb 2023 06:08:40 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
