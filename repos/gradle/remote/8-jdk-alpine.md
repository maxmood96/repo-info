## `gradle:8-jdk-alpine`

```console
$ docker pull gradle@sha256:d3bd83582a31e6e93f0be3478881889e3bdc5ae86676f9f5c5e853c63d039ab4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:8-jdk-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:43641515f2804d2fcee81dca6162b2f0434121669593ff94d8df40d58b2f491b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.4 MB (327360114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb088c915084bbaf9b0e237b0c24f935c37e5b87649e2806ede3cc57dbedbab8`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 30 Nov 2023 23:22:52 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Thu, 30 Nov 2023 23:22:52 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 07:11:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 01 Dec 2023 07:11:18 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Dec 2023 07:11:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Dec 2023 07:12:38 GMT
RUN set -eux;     apk add --no-cache         bash         fontconfig ttf-dejavu         java-cacerts         libretls zlib         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Fri, 01 Dec 2023 07:12:38 GMT
ENV JAVA_VERSION=jdk-17.0.9+9
# Fri, 01 Dec 2023 07:12:47 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='c2a571a56e5bd3f30956b17b048880078c7801ed9e8754af6d1e38b9176059a9';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.9%2B9/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.9_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Fri, 01 Dec 2023 07:12:50 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Fri, 01 Dec 2023 07:12:50 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Fri, 01 Dec 2023 07:12:50 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Fri, 01 Dec 2023 07:12:50 GMT
CMD ["jshell"]
# Fri, 01 Dec 2023 09:53:56 GMT
CMD ["gradle"]
# Fri, 01 Dec 2023 09:53:56 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 18 Jan 2024 19:02:22 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 18 Jan 2024 19:02:22 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 18 Jan 2024 19:02:22 GMT
WORKDIR /home/gradle
# Thu, 18 Jan 2024 19:02:25 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Thu, 18 Jan 2024 19:02:25 GMT
ENV GRADLE_VERSION=8.5
# Thu, 18 Jan 2024 19:02:26 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Thu, 18 Jan 2024 19:02:31 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Thu, 18 Jan 2024 19:02:31 GMT
USER gradle
# Thu, 18 Jan 2024 19:02:33 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Thu, 18 Jan 2024 19:02:33 GMT
USER root
```

-	Layers:
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5820a814e8c90e2b86457ad1da29a79516ae242489d7bf67ea216d150c1efdc`  
		Last Modified: Fri, 01 Dec 2023 07:15:58 GMT  
		Size: 13.1 MB (13141060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec533064323b9596a959f12635ca06c4ee0965ca1b44257c3e65fca566a63512`  
		Last Modified: Fri, 01 Dec 2023 07:16:08 GMT  
		Size: 144.1 MB (144111197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb67c9837c6a071b2db6278557e6372b3cd1049dbf05b46970ebcd3462a542a2`  
		Last Modified: Fri, 01 Dec 2023 07:15:57 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f3195d8bdd8ee99ecf37259027c679b512a94c32c26bc7e461556da58f8d99`  
		Last Modified: Fri, 01 Dec 2023 07:15:57 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069c961a83ea5c3377bcc7949caa74c2327f30260c3d4007d798c1abe479033c`  
		Last Modified: Thu, 18 Jan 2024 19:12:20 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9720038b4eb9579c8a03f70049bd44b23a5846ed6e427fb1b2a5d86ef87cc1f1`  
		Last Modified: Thu, 18 Jan 2024 19:12:25 GMT  
		Size: 34.2 MB (34158581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04e9a64996e2b456a9538a540487ac4feca9ffd689c6dfb1f93c03f1673066ac`  
		Last Modified: Thu, 18 Jan 2024 19:12:27 GMT  
		Size: 132.5 MB (132544441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c74cf42ee1d40585bfce9376a7034dc675d0c18451dda46ab3c3b1a99371152a`  
		Last Modified: Thu, 18 Jan 2024 19:12:20 GMT  
		Size: 168.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
