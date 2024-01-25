## `gradle:8-jdk21-alpine`

```console
$ docker pull gradle@sha256:a31b66b74fc29a95fb967b860748d8609bf816d4dd6bdf29d68e06258736ac8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:8-jdk21-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:40640e039c4731c63093759ce39f5d29fdd90efb179f781fef9d7ce3faceee42
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.5 MB (342530443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e0b8ef2f301d233eaa54ea66aca24f9fb41708e11dfb0a9cd672e89feb774d1`
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
# Wed, 24 Jan 2024 20:37:20 GMT
ENV JAVA_VERSION=jdk-21.0.2+13
# Wed, 24 Jan 2024 20:37:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='ae933ea8eeb4a077f19277842ba95ba93d29177e44d53cec7a98afd3b9abb2c3';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        amd64|x86_64)          ESUM='f1aef3652dd52778e81eb4897a88a34e38ca0159d22f160f7205e69907a0f14d';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.2%2B13/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.2_13.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Wed, 24 Jan 2024 20:37:34 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Wed, 24 Jan 2024 20:37:34 GMT
COPY file:aaf8d8da6065d3bd1ae04bf3c61d0adc8b6aa74964f19b57d4566fe5ec22ae14 in /__cacert_entrypoint.sh 
# Wed, 24 Jan 2024 20:37:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Wed, 24 Jan 2024 20:37:35 GMT
CMD ["jshell"]
# Wed, 24 Jan 2024 23:17:54 GMT
CMD ["gradle"]
# Wed, 24 Jan 2024 23:17:54 GMT
ENV GRADLE_HOME=/opt/gradle
# Wed, 24 Jan 2024 23:17:54 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle     && chmod -R o+rwx /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Wed, 24 Jan 2024 23:17:55 GMT
VOLUME [/home/gradle/.gradle]
# Wed, 24 Jan 2024 23:17:55 GMT
WORKDIR /home/gradle
# Wed, 24 Jan 2024 23:17:58 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Wed, 24 Jan 2024 23:17:58 GMT
ENV GRADLE_VERSION=8.5
# Wed, 24 Jan 2024 23:17:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Wed, 24 Jan 2024 23:18:04 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 24 Jan 2024 23:18:04 GMT
USER gradle
# Wed, 24 Jan 2024 23:18:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 24 Jan 2024 23:18:05 GMT
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
	-	`sha256:403c4d877b998762482a66a1422cf786267c9e5922268272b329bcc52faeaa41`  
		Last Modified: Wed, 24 Jan 2024 20:49:10 GMT  
		Size: 158.6 MB (158613071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73eef162f2708025567f5ef6c94ecbeb2d6e85e4343cc96da83093367a375ca`  
		Last Modified: Wed, 24 Jan 2024 20:48:58 GMT  
		Size: 178.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d13e04fe5ba030085094d071302edb0ad176664bf8e7361bc4fed4004c6117`  
		Last Modified: Wed, 24 Jan 2024 20:48:58 GMT  
		Size: 714.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be6f23c5f3d5313d20d6be1f0d9e42788f94b64c63c48710f34a92d2c6f9b049`  
		Last Modified: Wed, 24 Jan 2024 23:27:26 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbe857eeda4bd1c62eab9c8f9c746c04328b73185600b504d1ba748bcf319575`  
		Last Modified: Wed, 24 Jan 2024 23:27:32 GMT  
		Size: 34.8 MB (34824122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a68a48daae7c500bd44422f99b184b12e16436aaeb7fb00ef973293a6bc9214b`  
		Last Modified: Wed, 24 Jan 2024 23:27:36 GMT  
		Size: 132.5 MB (132544352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d805286570b4803c5a2600ff272d17fc952c1b7e87c32af6ccd4a2b8ac7f51d7`  
		Last Modified: Wed, 24 Jan 2024 23:27:26 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
