## `gradle:jdk18-alpine`

```console
$ docker pull gradle@sha256:96e1d9b57cb32665757b6f4fb3195dd9f84279875f96be43fe4e9e97fe2fcf3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk18-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:87b79a68838c961b5e8410b5fa8651dcfd73920de5c0576a53d2006488574b88
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **365.1 MB (365068115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0f15d3bc962de45ed691b6aea4b27852fb63616c4fb50a94f9ee597687e9448`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:30:24 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 10 Aug 2022 01:30:26 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 10 Aug 2022 01:32:54 GMT
ENV JAVA_VERSION=jdk-18.0.2+9
# Wed, 10 Aug 2022 01:33:24 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='045670342a036fff98b2ee90279ed923dc8c92bebe6227a2a60f64ca84f4f7c8';          BINARY_URL='https://github.com/adoptium/temurin18-binaries/releases/download/jdk-18.0.2%2B9/OpenJDK18U-jdk_x64_alpine-linux_hotspot_18.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 10 Aug 2022 01:33:25 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 10 Aug 2022 01:33:26 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 10 Aug 2022 01:33:26 GMT
CMD ["jshell"]
# Wed, 10 Aug 2022 06:15:13 GMT
CMD ["gradle"]
# Wed, 10 Aug 2022 06:15:13 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 10 Aug 2022 06:15:14 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 10 Aug 2022 06:15:14 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 10 Aug 2022 06:15:14 GMT
WORKDIR /home/gradle
# Wed, 10 Aug 2022 06:15:18 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Wed, 10 Aug 2022 06:15:18 GMT
ENV GRADLE_VERSION=7.5.1
# Wed, 10 Aug 2022 06:15:18 GMT
ARG GRADLE_DOWNLOAD_SHA256=f6b8596b10cce501591e92f229816aa4046424f3b24d771751b06779d58c8ec4
# Wed, 10 Aug 2022 06:15:24 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f6b8596b10cce501591e92f229816aa4046424f3b24d771751b06779d58c8ec4
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:878a9af9475f057a355a16521c6da6195d134a78707eb526021019fe67b702b5`  
		Last Modified: Wed, 10 Aug 2022 01:35:31 GMT  
		Size: 12.1 MB (12050079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fb9fee1c1338ebe463c13e4d7ece3e5f95cba558caa64493ce1f6cac2da0e91`  
		Last Modified: Wed, 10 Aug 2022 01:38:09 GMT  
		Size: 192.9 MB (192897563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7d5b48ab638eb446c579d5c6d665eb01c2b6816d0f7d043286e500bb729184`  
		Last Modified: Wed, 10 Aug 2022 01:37:54 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2b01500f0c823fcfb925fd26f52b0ad7ffd01583ae4222a9f5037e0c4c9d38`  
		Last Modified: Wed, 10 Aug 2022 06:19:30 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f88e376f1f51bd2ee181296116f72cbf0cd847f28520adbd420ae7a12f5a84`  
		Last Modified: Wed, 10 Aug 2022 06:19:36 GMT  
		Size: 36.7 MB (36655069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c69c156162ef1270c97e23633f7844668103cd22ccf35d48054742a3436f029`  
		Last Modified: Wed, 10 Aug 2022 06:19:37 GMT  
		Size: 120.7 MB (120657859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
