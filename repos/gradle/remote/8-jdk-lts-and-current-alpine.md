## `gradle:8-jdk-lts-and-current-alpine`

```console
$ docker pull gradle@sha256:8465de6012a1eb2733838b2784d731a4790e7077c1fb1dd2038cc0afc3211c18
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `gradle:8-jdk-lts-and-current-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:d539faa95e802b4a5ac45cbd176c4a31f69c79446372461dd5c8fbc7277077a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **511.4 MB (511433959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70b31a2e39ec08863ad4a0ffc7f2bbdda8e0920a2bee451ba225e089db8ad6ab`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 06 Sep 2024 22:20:07 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Fri, 06 Sep 2024 22:20:07 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Sat, 28 Sep 2024 00:46:05 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 28 Sep 2024 00:46:05 GMT
WORKDIR /home/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_VERSION=8.10.2
# Sat, 28 Sep 2024 00:46:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER gradle
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER root
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591c34627c847892ee87160ccb0488eb4484039dd04d400e9e86561f15459495`  
		Last Modified: Fri, 06 Sep 2024 22:44:13 GMT  
		Size: 14.0 MB (14032627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf8156c97e09482c8570965c0b9238fec4fef282a569e89f67a4eb990894ee6`  
		Last Modified: Fri, 06 Sep 2024 22:45:05 GMT  
		Size: 158.8 MB (158815391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14b0721dd94269153e4f5994aac8f72c2c57e0f1a0a464fa53bee6d993fed5e1`  
		Last Modified: Fri, 06 Sep 2024 22:44:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcd5a714946cb14973166aaf3ad39335cd7fd14cad658b8ceb9026cd7cb72ee`  
		Last Modified: Fri, 06 Sep 2024 22:44:52 GMT  
		Size: 2.1 KB (2106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b84ddd60344444676b25d22eec97108aebf1657325a542b53dc8a1a8f4c9d09`  
		Last Modified: Mon, 30 Sep 2024 21:56:11 GMT  
		Size: 165.5 MB (165477353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59ab4b30cf64e50fa9ac5ba07e1e40f0ec678e8c6e3f584ecde4f0871753cd67`  
		Last Modified: Mon, 30 Sep 2024 21:56:09 GMT  
		Size: 152.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90917d913500492f356cc5425953423dc0b374a1f157eb568b23ad4d1a2191a1`  
		Last Modified: Mon, 30 Sep 2024 21:56:09 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f80956c8ff7cc735fc350e20302c8fe426e6855811ad03b0ee7c8e40be26bce`  
		Last Modified: Mon, 30 Sep 2024 21:56:10 GMT  
		Size: 32.8 MB (32750604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2039fd2f50f36dd432d4a3ef8d02deeee87ed74dcb9f06005ed8cf284eefcf92`  
		Last Modified: Mon, 30 Sep 2024 21:56:12 GMT  
		Size: 136.7 MB (136730291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b088ddbd9010b2db902627accc88d9706c350dff30b257739be990956178771`  
		Last Modified: Mon, 30 Sep 2024 21:56:10 GMT  
		Size: 286.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:bb9ebcba7f26be56f861d4a48caa723e676f11f00067a3949b5bbd087961c381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 MB (3411352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bd253187cb4bfeb886dc26e2ae1788ea23f1d9044e6888c8c3f585dc0223dbf`

```dockerfile
```

-	Layers:
	-	`sha256:f596d2f8e2cbedffc5e8841eb292d3dfc78aa0e6af88c7dd0f7ba544da314fcd`  
		Last Modified: Mon, 30 Sep 2024 21:56:09 GMT  
		Size: 3.4 MB (3380757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ccaede78d4eac162a44b642fb194ee9fefa89decf9545cbd401942394ffb647`  
		Last Modified: Mon, 30 Sep 2024 21:56:09 GMT  
		Size: 30.6 KB (30595 bytes)  
		MIME: application/vnd.in-toto+json

### `gradle:8-jdk-lts-and-current-alpine` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:06aab3546ecbb64c27b7a50377bfdf5c6b1e53d67b4cdaaf674c5226377ae599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **508.0 MB (507960701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f02d8333cfc4789d7d5ecf2397bd6a95df74e25303ba13336eba76fb7e5ae516`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
CMD ["/bin/sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 22 Aug 2024 07:58:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Aug 2024 07:58:33 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     apk add --no-cache         fontconfig ttf-dejavu         ca-certificates p11-kit-trust         musl-locales musl-locales-lang         binutils         tzdata         coreutils         openssl     ;     rm -rf /var/cache/apk/* # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENV JAVA_VERSION=jdk-21.0.4+7
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64)          ESUM='849c6d5a62a1f3dc2a3d2d7be07ffda089d35b862f6160b2a288c0408c2d8be8';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        x86_64)          ESUM='8fa232fc9de5a861c1a6b0cbdc861d0b0a2bdbdd27da53d991802a460a7f0973';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21.0.4%2B7/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21.0.4_7.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip; # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete." # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
COPY --chmod=755 entrypoint.sh /__cacert_entrypoint.sh # buildkit
# Thu, 22 Aug 2024 07:58:33 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 22 Aug 2024 07:58:33 GMT
CMD ["jshell"]
# Sat, 28 Sep 2024 00:46:05 GMT
COPY /opt/java/openjdk /opt/java/openjdk23 # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && ln -s /opt/java/openjdk /opt/java/openjdk21 # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV JAVA_CURRENT_HOME=/opt/java/openjdk23
# Sat, 28 Sep 2024 00:46:05 GMT
ENV JAVA_LTS_HOME=/opt/java/openjdk21
# Sat, 28 Sep 2024 00:46:05 GMT
CMD ["gradle"]
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle       && echo "Ensuring Gradle detects installed JDKs"    && echo "org.gradle.java.installations.auto-detect=false" > /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.auto-download=false" >> /home/gradle/.gradle/gradle.properties    && echo "org.gradle.java.installations.fromEnv=JAVA_LTS_HOME,JAVA_CURRENT_HOME" >> /home/gradle/.gradle/gradle.properties # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 28 Sep 2024 00:46:05 GMT
WORKDIR /home/gradle
# Sat, 28 Sep 2024 00:46:05 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
ENV GRADLE_VERSION=8.10.2
# Sat, 28 Sep 2024 00:46:05 GMT
ARG GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER gradle
# Sat, 28 Sep 2024 00:46:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=31c55713e40233a8303827ceb42ca48a47267a0ad4bab9177123121e71524c26
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version # buildkit
# Sat, 28 Sep 2024 00:46:05 GMT
USER root
```

-	Layers:
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8a2d3622211b600f84f1b27f8913afa35a6719e1ddde90ee5afb4bc8b95868`  
		Last Modified: Fri, 06 Sep 2024 23:28:36 GMT  
		Size: 14.4 MB (14361804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08647f9de401eb33fe1c2f4f352dbebe5ec7ef1fd5027625352d378c0360a987`  
		Last Modified: Fri, 06 Sep 2024 23:28:44 GMT  
		Size: 156.7 MB (156728954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee7659a4477f6becb82c0fd7f718ae436602ca24d57684440fe89d3e308137fd`  
		Last Modified: Fri, 06 Sep 2024 23:28:34 GMT  
		Size: 157.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2016bd617f1694a2d5a9bb7bf687d586a02ac91ef5b27ab5d83e84fd202ad9`  
		Last Modified: Fri, 06 Sep 2024 23:28:34 GMT  
		Size: 2.1 KB (2107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83cc50bc2b7d7adc074be2cbe9d9f1e9db6306f41037c0f6dd9ad74a036ef82`  
		Last Modified: Mon, 30 Sep 2024 22:13:30 GMT  
		Size: 163.3 MB (163268496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c1ecd4d17424c4a1f7aa486cd092bc66b0662d3ff2e9983ce9a42068a764aa`  
		Last Modified: Mon, 30 Sep 2024 22:13:25 GMT  
		Size: 153.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3513e0cb8ea439c0ef57f0e2b055613ac8e9890b3bd84a1192ed26f94fa2fdbd`  
		Last Modified: Mon, 30 Sep 2024 22:13:25 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87e0588e64b5d89f01f1774cbdd881c296eb71961a7ed97647c449c7393bded9`  
		Last Modified: Mon, 30 Sep 2024 22:13:27 GMT  
		Size: 32.8 MB (32779870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d5594a5d25e4c728faa2196e970377fbfd408b696735f1454efbdae4a5db925`  
		Last Modified: Mon, 30 Sep 2024 22:13:31 GMT  
		Size: 136.7 MB (136730043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf7fedbbdece84626566cc5261487255580dbc8d9e4c85d1d1e434748311f143`  
		Last Modified: Mon, 30 Sep 2024 22:13:26 GMT  
		Size: 291.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `gradle:8-jdk-lts-and-current-alpine` - unknown; unknown

```console
$ docker pull gradle@sha256:72c1a6e97cdd4e799eec176832180b2235937bba5ec34f7173ac3c3ef4de4e77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3515564 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fffd70142f3cdbaab1c1f8096004c78c21703020502a02bac520504e7fb4bf57`

```dockerfile
```

-	Layers:
	-	`sha256:27fb12401c6bfc065f69eb3f5e926598c417a6c9a3ec28083909c23d988aea9a`  
		Last Modified: Mon, 30 Sep 2024 22:13:26 GMT  
		Size: 3.5 MB (3484348 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d103862e5e485bc44a3f2d9b563f839cd11403eb37199a60d3af10236d98fca3`  
		Last Modified: Mon, 30 Sep 2024 22:13:25 GMT  
		Size: 31.2 KB (31216 bytes)  
		MIME: application/vnd.in-toto+json
