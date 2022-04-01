## `gradle:7-jdk11-alpine`

```console
$ docker pull gradle@sha256:56f96b1d3880588e5f5589f67edf922e1c99801a3c8119d61b5a0f59565ac95c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:7-jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:01fc6c2ac9ccc62da8584778ee1959846024455f998bafa6359749b4765b973b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347403483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9092a98c2d3f6bfd1b1dd76fbc634417202c6761d005068d8ba931c85ff55a7c`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 29 Mar 2022 00:19:36 GMT
ADD file:3b5a33c96fd3c10d0c438d907ce172903f7b2bde0f4e5107831e135ddf111b19 in / 
# Tue, 29 Mar 2022 00:19:36 GMT
CMD ["/bin/sh"]
# Tue, 29 Mar 2022 06:09:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 29 Mar 2022 06:09:17 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Tue, 29 Mar 2022 06:09:46 GMT
ENV JAVA_VERSION=jdk-11.0.14.1+1
# Tue, 29 Mar 2022 06:09:59 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='99e13a167ac27fac3dbfcc394a024fd9f4d84d24734ad5c250f97215d496ee36';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.14.1%2B1/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.14.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 29 Mar 2022 06:10:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 06:10:01 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 29 Mar 2022 06:10:01 GMT
CMD ["jshell"]
# Wed, 30 Mar 2022 13:28:31 GMT
CMD ["gradle"]
# Wed, 30 Mar 2022 13:28:32 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 30 Mar 2022 13:28:32 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 30 Mar 2022 13:28:32 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 30 Mar 2022 13:28:32 GMT
WORKDIR /home/gradle
# Wed, 30 Mar 2022 13:28:36 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Fri, 01 Apr 2022 17:21:05 GMT
ENV GRADLE_VERSION=7.4.2
# Fri, 01 Apr 2022 17:21:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
# Fri, 01 Apr 2022 17:21:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=29e49b10984e585d8118b7d0bc452f944e386458df27371b49b4ac1dec4b7fda
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:40e059520d199e1a1a259089077f2a0c879951c9a4540490bad3a0d7714c6ae7`  
		Last Modified: Mon, 28 Mar 2022 23:30:57 GMT  
		Size: 2.8 MB (2814512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8b72f2e4b8ed4ba22286a50d6f2bf2b7f79589f32f8c9de1f0e643014314af`  
		Last Modified: Tue, 29 Mar 2022 06:12:48 GMT  
		Size: 430.5 KB (430474 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5af124754ebe024a6e5a6fa50cbdbf9f1020648f8e63b65a160455a54cc7ff3`  
		Last Modified: Tue, 29 Mar 2022 06:13:38 GMT  
		Size: 192.9 MB (192891665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb133c64c3e2fd67ee497c9413f91a46986a425fabefb1c984dfff908dfda4a7`  
		Last Modified: Tue, 29 Mar 2022 06:13:25 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f17bd60073606f093bd237b0eda09297249143d92fb86408665839248d06c5`  
		Last Modified: Wed, 30 Mar 2022 13:30:26 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6f3e01ed78c3d156b319083ab30f1c560e945bf0fabeb96634e8bd95f93804b`  
		Last Modified: Wed, 30 Mar 2022 13:30:33 GMT  
		Size: 35.4 MB (35398399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c487b8003736ba4a2aaa2681294c5636669ad0c8b0120cb9631526367b23d47`  
		Last Modified: Fri, 01 Apr 2022 17:23:24 GMT  
		Size: 115.9 MB (115866945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
