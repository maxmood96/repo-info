## `gradle:jdk11-alpine`

```console
$ docker pull gradle@sha256:410b9da92a915b6f4414acf492d6594f894e0689793991f546cfcf441458d521
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `gradle:jdk11-alpine` - linux; amd64

```console
$ docker pull gradle@sha256:fb863c19ff5d0a1985cd1d66828cc38ab1d32eebf35265e3d15acff263c3144a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **320.7 MB (320746363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e45fa96bca79792fe79d021ddf31b00c629c71a02461c71c5bec45241271a4`
-	Entrypoint: `["\/__cacert_entrypoint.sh"]`
-	Default Command: `["gradle"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 02:50:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Oct 2023 02:50:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 02:50:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 30 Oct 2023 23:22:37 GMT
RUN set -eux;     apk add --no-cache         bash         fontconfig ttf-dejavu         java-cacerts         libretls zlib         musl-locales musl-locales-lang         tzdata     ;     rm -rf /var/cache/apk/*
# Mon, 30 Oct 2023 23:22:38 GMT
ENV JAVA_VERSION=jdk-11.0.21+9
# Mon, 30 Oct 2023 23:22:46 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='d5e2235d3707526f7c9ba3f0dc194e60d5dec33eceff2a2dcf9d874464cc0e9e';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.21%2B9/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.21_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     wget -O /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p "$JAVA_HOME";     tar --extract         --file /tmp/openjdk.tar.gz         --directory "$JAVA_HOME"         --strip-components 1         --no-same-owner     ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Mon, 30 Oct 2023 23:22:48 GMT
RUN set -eux;     echo "Verifying install ...";     fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java;     echo "javac --version"; javac --version;     echo "java --version"; java --version;     echo "Complete."
# Mon, 30 Oct 2023 23:22:48 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 30 Oct 2023 23:22:48 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 30 Oct 2023 23:22:49 GMT
CMD ["jshell"]
# Tue, 31 Oct 2023 05:21:25 GMT
CMD ["gradle"]
# Tue, 31 Oct 2023 05:21:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Oct 2023 05:21:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && addgroup --system --gid 1000 gradle     && adduser --system --ingroup gradle --uid 1000 --shell /bin/ash gradle     && mkdir /home/gradle/.gradle     && chown -R gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 31 Oct 2023 05:21:26 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Oct 2023 05:21:26 GMT
WORKDIR /home/gradle
# Tue, 31 Oct 2023 05:21:29 GMT
RUN set -o errexit -o nounset     && echo "Installing VCSes"     && apk add --no-cache       git       git-lfs       mercurial       subversion         && echo "Testing VCSes"     && which git     && which git-lfs     && which hg     && which svn
# Wed, 29 Nov 2023 23:45:47 GMT
ENV GRADLE_VERSION=8.5
# Wed, 29 Nov 2023 23:45:47 GMT
ARG GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
# Wed, 29 Nov 2023 23:45:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking Gradle download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum -c -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln -s "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle
# Wed, 29 Nov 2023 23:45:52 GMT
USER gradle
# Wed, 29 Nov 2023 23:45:54 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=9d926787066a081739e8200858338b4a69e837c3a821a33aca9db09dd4a41026
RUN set -o errexit -o nounset     && echo "Testing Gradle installation"     && gradle --version
# Wed, 29 Nov 2023 23:45:54 GMT
USER root
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b02a3a37ba0a441c23edb967d901e4af5b508796b983fbb71e14ad89db9a9999`  
		Last Modified: Mon, 30 Oct 2023 23:32:06 GMT  
		Size: 9.3 MB (9276545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a12e67e82faf020e769d46cccfc7f1620ccb86e04b4576b070512194641eb854`  
		Last Modified: Mon, 30 Oct 2023 23:32:15 GMT  
		Size: 140.5 MB (140484655 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43caa4ccd4f85f364bbf72014cc960dc6fb6703350eceaee77976cf6313c8a55`  
		Last Modified: Mon, 30 Oct 2023 23:32:04 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8800858de447fac23faff681df1122b67d784efb0ee850d3d9551bcb5e9b19f8`  
		Last Modified: Mon, 30 Oct 2023 23:32:04 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93174729fb9154c647b46c3b3a0514a6b72eaec36aac27e02010f1ef1ea0b356`  
		Last Modified: Tue, 31 Oct 2023 05:28:53 GMT  
		Size: 1.3 KB (1332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416e8b9ff71dca36af172e5f3dc2a72409c86e5f2473dfcb3bc86d9ac0d20fda`  
		Last Modified: Tue, 31 Oct 2023 05:28:59 GMT  
		Size: 35.0 MB (35036388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:573dd46ba3ab2be5b6e0b65d3ad931a40855d0f0f590b1d1869fb7c904a5fdf4`  
		Last Modified: Wed, 29 Nov 2023 23:50:59 GMT  
		Size: 132.5 MB (132544398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3e67beaa97b36cf3ddf6fcc1b0ed346e1497c01baf1dc4210d04bc6d804f65`  
		Last Modified: Wed, 29 Nov 2023 23:50:53 GMT  
		Size: 169.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
