## `gradle:jdk11-alpine`

```console
$ docker pull gradle@sha256:6892ca49e154a1740cec276312df99db9eeeb3f0d96e980620e81a0450c4f816
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:bf3aaada6a8ca92f9d57c9fb318eb3fc5646ba884ae6b34c65da3134677b7264
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.6 MB (365619066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5c07decb2ee0968a7adbc3c187a58346b8979180658204e9e89c0eb3a325e53`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Fri, 07 Oct 2022 16:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 07 Oct 2022 16:53:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 07 Oct 2022 16:53:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 07 Oct 2022 16:53:21 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Fri, 07 Oct 2022 16:53:57 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Fri, 07 Oct 2022 16:54:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='327b3bfd1c14e15bf6c7fb4d0c6c3f9406c1282a16e24b1424215d764f687cb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Fri, 07 Oct 2022 16:54:15 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 07 Oct 2022 16:54:15 GMT
CMD ["jshell"]
# Fri, 07 Oct 2022 17:31:16 GMT
CMD ["gradle"]
# Fri, 07 Oct 2022 17:31:16 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 07 Oct 2022 17:31:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 07 Oct 2022 17:31:17 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 07 Oct 2022 17:31:17 GMT
WORKDIR /home/gradle
# Fri, 07 Oct 2022 17:31:21 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Fri, 07 Oct 2022 17:31:21 GMT
ENV GRADLE_VERSION=7.5.1
# Fri, 07 Oct 2022 17:31:21 GMT
ARG GRADLE_DOWNLOAD_SHA256=f6b8596b10cce501591e92f229816aa4046424f3b24d771751b06779d58c8ec4
# Fri, 07 Oct 2022 17:31:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f6b8596b10cce501591e92f229816aa4046424f3b24d771751b06779d58c8ec4
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e5835cc7e6eb64b728c9694dd72d8aede877af0a2ec44f981847853af9abbf5`  
		Last Modified: Fri, 07 Oct 2022 16:57:51 GMT  
		Size: 12.0 MB (12041341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fba20fc96420980a5e92cbc17d7ed8001550d853c0f3a2d2edab1d439b9f8a12`  
		Last Modified: Fri, 07 Oct 2022 16:58:47 GMT  
		Size: 193.5 MB (193457737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3be129b993c212fc41b64fa2d86dc4b12ba9c94eaced404bab46dc0c9d72544a`  
		Last Modified: Fri, 07 Oct 2022 16:58:33 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8250c89a3b8810cd083c5795f9b0714f5c86a4e47828d3539c4f3cd39dfcbf3e`  
		Last Modified: Fri, 07 Oct 2022 17:34:53 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8683636229bb79f5d1ebf19b2093588d7049847a8c6470fc7946a571025587d3`  
		Last Modified: Fri, 07 Oct 2022 17:34:59 GMT  
		Size: 36.7 MB (36654533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:952d4bfb70cbc79f84e6d7092071c273f622026d0325a7698f175fa4a4326156`  
		Last Modified: Fri, 07 Oct 2022 17:35:00 GMT  
		Size: 120.7 MB (120657891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
