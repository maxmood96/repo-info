## `maven:3-eclipse-temurin-16-alpine`

```console
$ docker pull maven@sha256:e018855cde9c241a35439ebc98f10e1a2414808e303cdba4e6a3f157953522a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `maven:3-eclipse-temurin-16-alpine` - linux; amd64

```console
$ docker pull maven@sha256:32b8ff5782bffefe243f59fa1f256853c3da365573de6dfd9e0eb6cafb640fb4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.2 MB (220229342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311daf7e5f1b3aebf9be1d50d34829a547b5ef14fa1cd46ecb6aa13f261a8aac`
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
# Fri, 12 Nov 2021 22:10:50 GMT
ENV JAVA_VERSION=jdk-16.0.2+7
# Fri, 12 Nov 2021 22:11:05 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='85788b1a1f470ca7ddc576028f29abbc3bc3b08f82dd811a3e24371689d7dc0f';          BINARY_URL='https://github.com/adoptium/temurin16-binaries/releases/download/jdk-16.0.2%2B7/OpenJDK16U-jdk_x64_alpine-linux_hotspot_16.0.2_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 12 Nov 2021 22:11:06 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 22:11:07 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 12 Nov 2021 22:11:07 GMT
CMD ["jshell"]
# Tue, 14 Dec 2021 01:37:39 GMT
ARG MAVEN_VERSION=3.8.4
# Tue, 14 Dec 2021 01:37:39 GMT
ARG USER_HOME_DIR=/root
# Tue, 14 Dec 2021 01:37:39 GMT
ARG SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8
# Tue, 14 Dec 2021 01:37:39 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries
# Tue, 14 Dec 2021 01:37:41 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN apk add --no-cache curl tar bash procps
# Tue, 14 Dec 2021 01:37:43 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.4/binaries MAVEN_VERSION=3.8.4 SHA=a9b2d825eacf2e771ed5d6b0e01398589ac1bfa4171f36154d1b5787879605507802f699da6f7cfc80732a5282fd31b28e4cd6052338cbef0fa1358b48a5e3c8 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Tue, 14 Dec 2021 01:37:43 GMT
ENV MAVEN_HOME=/usr/share/maven
# Tue, 14 Dec 2021 01:37:43 GMT
ENV MAVEN_CONFIG=/root/.m2
# Tue, 14 Dec 2021 01:37:44 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Tue, 14 Dec 2021 01:37:44 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Tue, 14 Dec 2021 01:37:44 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Tue, 14 Dec 2021 01:37:44 GMT
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
	-	`sha256:127fcb40ccb64f778eb06fb2a1957c35e3abfd924f410781d933b4d3b8576139`  
		Last Modified: Fri, 12 Nov 2021 22:14:08 GMT  
		Size: 205.5 MB (205473576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee43c163f4268f6c2312f341573fbb51f84104a1a8455dcb61bc8fd7876a0d43`  
		Last Modified: Fri, 12 Nov 2021 22:13:49 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13bb4714c55d81a8b8a5fc53dae415e9413740c1e021800a6b531f0baab58723`  
		Last Modified: Tue, 14 Dec 2021 01:40:05 GMT  
		Size: 2.4 MB (2391520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c7f00bd51fdfcde97b75f9b6a7af3b754091e0c2c08427a655ffce47059ec1a`  
		Last Modified: Tue, 14 Dec 2021 01:40:05 GMT  
		Size: 9.1 MB (9109811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580ca0bcb79e72f3ebf6c24e8a545ad489b9bc1f452c1d6131a5512c9f6ab1cb`  
		Last Modified: Tue, 14 Dec 2021 01:40:04 GMT  
		Size: 853.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e01915334a075221e34c0a6310cb1f87b6fb99517d9e1758c94621e492c8b5`  
		Last Modified: Tue, 14 Dec 2021 01:40:04 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
