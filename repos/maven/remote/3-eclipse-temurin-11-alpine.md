## `maven:3-eclipse-temurin-11-alpine`

```console
$ docker pull maven@sha256:346b93e4d4035658052d42a2c3b4f220223059cdbf1bcf1365422f60b5744463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-11-alpine` - linux; amd64

```console
$ docker pull maven@sha256:b7cfcf2b639fbff5d1fcb3753d7b3fe37950c97e6bf0108a249dedc4ec4a9248
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **207.5 MB (207497673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ecbdd225969c9e7194a8e1fea5815fe103f48c1663be5d495492d3388ea5eff`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 22:10:12 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 12 Nov 2021 22:10:13 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Fri, 12 Nov 2021 22:10:13 GMT
ENV JAVA_VERSION=jdk-11.0.13+8
# Fri, 12 Nov 2021 22:10:26 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='4216543c8eaa4b10475bbacb15bbda41e04ec5c8c57424b3303f60c36b8b362d';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.13%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.13_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 12 Nov 2021 22:10:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 22:10:28 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 12 Nov 2021 22:10:28 GMT
CMD ["jshell"]
# Tue, 14 Dec 2021 01:37:29 GMT
ARG MAVEN_VERSION=3.8.4
# Tue, 14 Dec 2021 01:37:29 GMT
ARG USER_HOME_DIR=/root
# Tue, 14 Dec 2021 01:37:29 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Tue, 14 Dec 2021 01:37:30 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Tue, 14 Dec 2021 01:37:31 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apk add --no-cache curl tar bash procps
# Tue, 14 Dec 2021 01:37:33 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 14 Dec 2021 01:37:34 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 14 Dec 2021 01:37:34 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 14 Dec 2021 01:37:34 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 14 Dec 2021 01:37:34 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 14 Dec 2021 01:37:34 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 14 Dec 2021 01:37:35 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56981b1bb25bf90c21f6060c91c15dbc4a3d4376abc16e9975ef475bc8561710`  
		Last Modified: Fri, 12 Nov 2021 22:12:51 GMT  
		Size: 430.1 KB (430083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b97623027cff394637ceb699001f714be6f2495ab2e0cfea545e1cfe4f9f2656`  
		Last Modified: Fri, 12 Nov 2021 22:13:10 GMT  
		Size: 192.7 MB (192741917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6fc9c4c02373f27144b7c6fb5c6d177b1a967cb562d4da0540641faa1d41f61`  
		Last Modified: Fri, 12 Nov 2021 22:12:50 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0981adddd7815a59ac5df35c81299b0912408c1134289d6672a59527c17933b4`  
		Last Modified: Tue, 14 Dec 2021 01:39:50 GMT  
		Size: 2.4 MB (2391514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f423cdae3c06d7758be6eec2e4408b5d2fbcf3c4fddb4a20b842697d2348961d`  
		Last Modified: Tue, 14 Dec 2021 01:39:50 GMT  
		Size: 9.1 MB (9109805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3228eaee3b1e3be96c3bb76986d81123d193941b9235fcb72c3f28db2eb965`  
		Last Modified: Tue, 14 Dec 2021 01:39:49 GMT  
		Size: 854.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:155463f767d717f8b81918d4dc50e9d751b27f1674d2069677ea151a1d17d71c`  
		Last Modified: Tue, 14 Dec 2021 01:39:49 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
