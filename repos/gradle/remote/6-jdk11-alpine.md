## `gradle:6-jdk11-alpine`

```console
$ docker pull gradle@sha256:8e9d9e6af199ac8d07afdad19c9cf055189be44b67ca3bbd1c40858325284923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:6-jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:7998078a5caf9473cc50611ea553eb2d6f49e33d879db232bdf2c9f607fe5d16
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.2 MB (339160761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d018e135484bce2c1d34487dcec957eb1e567ed74b14ef77efff906a287fdea`
-	Default Command: `["gradle"]`

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
# Sat, 13 Nov 2021 13:58:45 GMT
CMD ["gradle"]
# Sat, 13 Nov 2021 13:58:46 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 13 Nov 2021 13:58:46 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup -S -g 1000 gradle     && adduser -D -S -G gradle -u 1000 -s /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 13 Nov 2021 13:58:47 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 13 Nov 2021 13:58:47 GMT
WORKDIR /home/gradle
# Sat, 13 Nov 2021 13:58:50 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Sat, 13 Nov 2021 13:59:22 GMT
ENV GRADLE_VERSION=6.9.1
# Sat, 13 Nov 2021 13:59:22 GMT
ARG GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
# Sat, 13 Nov 2021 13:59:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
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
	-	`sha256:7fc5a5baac0653a1eb8e78151566808ed8be09dc553b133131a293a22fc6369d`  
		Last Modified: Sat, 13 Nov 2021 14:00:43 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e98fde214678c5a23bc98bb4a185cbb05e237ebd5f86026f1b6058f8d5dd88b2`  
		Last Modified: Sat, 13 Nov 2021 14:00:49 GMT  
		Size: 35.5 MB (35474503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace6794ed815c56833850f21a852ce3b64173248d478e610689cff7afb5e7127`  
		Last Modified: Sat, 13 Nov 2021 14:02:09 GMT  
		Size: 107.7 MB (107689790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
