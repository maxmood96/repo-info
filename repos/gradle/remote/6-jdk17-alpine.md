## `gradle:6-jdk17-alpine`

```console
$ docker pull gradle@sha256:03a85a32884095ef947e74dac8f48aec9feb7379459276e9d19d760e6c6f2bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:6-jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:18bbf252440e36ee0c60adb7ca3e779c94bc4c2636c99293ab75874320f215ec
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **338.3 MB (338274172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3626b4a34820df1c5f108276ea71790764753c0501dd666250259d81b5f541`
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
# Fri, 12 Nov 2021 22:11:15 GMT
ENV JAVA_VERSION=jdk-17.0.1+12
# Fri, 12 Nov 2021 22:11:37 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='da4845987b3348da14338a0620ef7db25870e27670e82baebcc367fa9d17c7de';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.1%2B12/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.1_12.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 12 Nov 2021 22:11:38 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Nov 2021 22:11:39 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 12 Nov 2021 22:11:39 GMT
CMD ["jshell"]
# Sat, 13 Nov 2021 13:59:03 GMT
CMD ["gradle"]
# Sat, 13 Nov 2021 13:59:03 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 13 Nov 2021 13:59:04 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup -S -g 1000 gradle     && adduser -D -S -G gradle -u 1000 -s /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 13 Nov 2021 13:59:04 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 13 Nov 2021 13:59:04 GMT
WORKDIR /home/gradle
# Sat, 13 Nov 2021 13:59:08 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Sat, 13 Nov 2021 13:59:33 GMT
ENV GRADLE_VERSION=6.9.1
# Sat, 13 Nov 2021 13:59:33 GMT
ARG GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
# Sat, 13 Nov 2021 13:59:38 GMT
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
	-	`sha256:eb6d985b90eeb385a832ce914b0c45cb9557ec40b835c335c57e656875044d50`  
		Last Modified: Fri, 12 Nov 2021 22:14:39 GMT  
		Size: 191.9 MB (191855171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:718042d8f3f27fd9ebc645c0428ea7a7cbfc517363da21fa72094177ab6404b1`  
		Last Modified: Fri, 12 Nov 2021 22:14:23 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b910684fa1f2c55dfc3eb80f70e3734f2863d46e5a6c9bf97d10a7cfed23048`  
		Last Modified: Sat, 13 Nov 2021 14:01:11 GMT  
		Size: 1.3 KB (1325 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc48af06debdc2bdb481e9763eea23caed162fed46f44c2761cc426f59e1017f`  
		Last Modified: Sat, 13 Nov 2021 14:01:17 GMT  
		Size: 35.5 MB (35474523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25e107a035ac27807b7b4d6717005d743ec48922a2ef92b43d7db667882e3f27`  
		Last Modified: Sat, 13 Nov 2021 14:02:32 GMT  
		Size: 107.7 MB (107689928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
