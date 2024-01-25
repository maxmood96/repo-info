## `gradle:8-jdk17-alpine`

```console
$ docker pull gradle@sha256:7086984f52afe8f06d81e081f11e7bebb20ac68bd3d4d5704534aa82c4197bd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:8-jdk17-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:4a3688f6cfdb6fb9479b3f0323d6216af9387d711b6eb9f30534e3e912f2cbb4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.1 MB (328059991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7107207b121b2ed71dd75dba763c812959f4d02b993281cc7afc28605cd5fe0`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Wed, 24 Jan 2024 20:31:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 24 Jan 2024 20:31:02 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jan 2024 20:31:02 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 24 Jan 2024 20:35:02 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata     ;     rm -rf /var/cache/apk/*
# Wed, 24 Jan 2024 20:35:02 GMT
ENV JAVA_VERSION=jdk-17.0.10+7
# Wed, 24 Jan 2024 20:35:12 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='ce4085548f73ec97fa870de3f7da87634b4cbbf9753600365e2e0b255585e7e1';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.10%2B7/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.10_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 24 Jan 2024 20:35:14 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:35:15 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:35:15 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 20:35:15 GMT
CMD ["jshell"]
# Wed, 24 Jan 2024 23:17:08 GMT
CMD ["gradle"]
# Wed, 24 Jan 2024 23:17:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 24 Jan 2024 23:17:08 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 24 Jan 2024 23:17:08 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 24 Jan 2024 23:17:09 GMT
WORKDIR /home/gradle
# Wed, 24 Jan 2024 23:17:12 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Wed, 24 Jan 2024 23:17:12 GMT
ENV GRADLE_VERSION=8.5
# Wed, 24 Jan 2024 23:17:12 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Wed, 24 Jan 2024 23:17:17 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 24 Jan 2024 23:17:18 GMT
USER gradle
# Wed, 24 Jan 2024 23:17:19 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 24 Jan 2024 23:17:19 GMT
USER root
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dbd32a74211c33dc91f4cd7a11dcd5977fcc3b3b6fe8b435951a5341b744d80`  
		Last Modified: Wed, 24 Jan 2024 20:45:45 GMT  
		Size: 13.1 MB (13138023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f620a95a97da35c1f059cd9771a9c1b941212fcffde401d5ce27bda15d82a74d`  
		Last Modified: Wed, 24 Jan 2024 20:45:54 GMT  
		Size: 144.1 MB (144142412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5220a570af7bb9f2b603b0556007fd0bd0e17ea698bbf0a859a6c758fe314d8`  
		Last Modified: Wed, 24 Jan 2024 20:45:43 GMT  
		Size: 177.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a246d64bf18b910810843e6f4ddf5767d9924aa91d5232e4882aad23cffc3c62`  
		Last Modified: Wed, 24 Jan 2024 20:45:43 GMT  
		Size: 717.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c919b908474724f7e4af0c5118f49bbb629ae582368d9775e1757dacec4508ca`  
		Last Modified: Wed, 24 Jan 2024 23:26:07 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72856e1554656937613f2cdf331ffafb922c5427e2ec114cccd62ef363b41389`  
		Last Modified: Wed, 24 Jan 2024 23:26:12 GMT  
		Size: 34.8 MB (34824288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c87b1ada744c7a22717c59f3ada36eb0b201cc58fa82d2d8a5d66ac2135f71f`  
		Last Modified: Wed, 24 Jan 2024 23:26:14 GMT  
		Size: 132.5 MB (132544393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a7e4401ad5405a9cf218149db4f43c33e11c409266ef47ea9817c1ece0d6bf1`  
		Last Modified: Wed, 24 Jan 2024 23:26:07 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
