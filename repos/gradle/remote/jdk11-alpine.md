## `gradle:jdk11-alpine`

```console
$ docker pull gradle@sha256:a79645842e509fb93e8db6efa1b78fb39d34c21db3179571400d26d25e452fec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:2bf5e2ac2729aa48deb9824dab62ee993ef00894418ddb482f1600e633ac6df4
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.4 MB (364352356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01beac8ddd7deab3b0a410b4fd150c2af51c692f3dc02e94e627bf7ab7d98ac7`
-	Default Command: `["gradle"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:40:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Jan 2023 17:40:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 17:40:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Jan 2023 17:40:11 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 09 Jan 2023 17:40:44 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Mon, 09 Jan 2023 17:40:57 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='774d5955c09893dda14e3eb0fd3e239a6b2cec58615fcf4ec68747260b6e1cc1';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Mon, 09 Jan 2023 17:41:00 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 09 Jan 2023 17:41:00 GMT
CMD ["jshell"]
# Mon, 09 Jan 2023 21:41:29 GMT
CMD ["gradle"]
# Mon, 09 Jan 2023 21:41:29 GMT
ENV GRADLE_HOME=/opt/gradle
# Mon, 09 Jan 2023 21:41:30 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Mon, 09 Jan 2023 21:41:30 GMT
VOLUME [/home/gradle/.gradle]
# Mon, 09 Jan 2023 21:41:30 GMT
WORKDIR /home/gradle
# Mon, 09 Jan 2023 21:41:33 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Mon, 09 Jan 2023 21:41:34 GMT
ENV GRADLE_VERSION=7.6
# Mon, 09 Jan 2023 21:41:34 GMT
ARG GRADLE_DOWNLOAD_SHA256=7ba68c54029790ab444b39d7e293d3236b2632631fb5f2e012bb28b4ff669e4b
# Mon, 09 Jan 2023 21:41:39 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=7ba68c54029790ab444b39d7e293d3236b2632631fb5f2e012bb28b4ff669e4b
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e3b32ee5a149e3ccb99051cdb52e96e11488293cdf72ee88168c88dd335c7`  
		Last Modified: Mon, 09 Jan 2023 17:44:40 GMT  
		Size: 12.0 MB (12020134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757b01b0b48f99a2f5e239f173b15678e8f1c1c91cb98fa568e12ed3ccaaeafe`  
		Last Modified: Mon, 09 Jan 2023 17:45:32 GMT  
		Size: 193.8 MB (193812585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ddd76e48fe00d19e510bc7b4b236ab01963c83cc619d3ff619c87c5f67603813`  
		Last Modified: Mon, 09 Jan 2023 17:45:18 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581c3109323a53d03ad2ba7f6c46f7246b6f4255602723036ae0d998946bf7cd`  
		Last Modified: Mon, 09 Jan 2023 21:44:51 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eac06ead66a95406037ebbc823924b3e3d02bf6b8fcd9ac0d06f547acf17c6e0`  
		Last Modified: Mon, 09 Jan 2023 21:44:56 GMT  
		Size: 33.1 MB (33090414 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba0a6021d606a20b3ecabf96870ae8e1dda669784c14b52e73e7a2f4ea2b221e`  
		Last Modified: Mon, 09 Jan 2023 21:44:57 GMT  
		Size: 122.1 MB (122057090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
