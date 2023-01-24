## `gradle:6-jdk11-focal`

```console
$ docker pull gradle@sha256:e5a73c04254dafe6730c0a32a2a7f887367cd643598cbc27f1b266c32e65f48e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6-jdk11-focal` - linux; amd64

```console
$ docker pull gradle@sha256:530cd15a876d73f9ab0d991814a971d79da7a1756f2a8e89bc320fc0c5d809eb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **416.4 MB (416377265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd0bd198ab7030c48731012944c9ee52a7d6ff9d14e293b9a738c3c529e8553c`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 Dec 2022 01:20:21 GMT
ADD file:9d282119af0c42bc823c95b4192a3350cf2cad670622017356dd2e637762e425 in / 
# Fri, 09 Dec 2022 01:20:21 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 01:42:10 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 01:42:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 01:42:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 01:42:42 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 01:44:09 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 09 Dec 2022 01:44:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d18b5dd73fce9edd5c58f623a1173f9ee2d45023836b8753b96beae51673a432';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='9ff3b4bd2bac18fb39f3356148efa2dc710ac029e12dc8f18ea1fe6be23bf299';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='18c636bd103e240d29cdb30d7867720ea9fb9ff7c645738bfb4d5b8027269263';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eb861db1433ddc1b89f170b789fafde282f137218d6d985fb5c2003e4ff44984';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b8d46ed08ef4859476fe6421a7690d899ed83dce63f13fd894f994043177ef3c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Dec 2022 01:44:20 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 09 Dec 2022 01:44:20 GMT
CMD ["jshell"]
# Fri, 09 Dec 2022 08:20:34 GMT
CMD ["gradle"]
# Fri, 09 Dec 2022 08:20:34 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 09 Dec 2022 08:20:34 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 09 Dec 2022 08:20:34 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 09 Dec 2022 08:20:35 GMT
WORKDIR /home/gradle
# Fri, 09 Dec 2022 08:20:53 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 09 Dec 2022 08:23:27 GMT
ENV GRADLE_VERSION=6.9.3
# Fri, 09 Dec 2022 08:23:27 GMT
ARG GRADLE_DOWNLOAD_SHA256=dcf350b8ae1aa192fc299aed6efc77b43825d4fedb224c94118ae7faf5fb035d
# Fri, 09 Dec 2022 08:23:32 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=dcf350b8ae1aa192fc299aed6efc77b43825d4fedb224c94118ae7faf5fb035d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:846c0b181fff0c667d9444f8378e8fcfa13116da8d308bf21673f7e4bea8d580`  
		Last Modified: Thu, 08 Dec 2022 13:18:11 GMT  
		Size: 28.6 MB (28576882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9923132fe6ab2c95fb9e2363f361139b8e50b7264d78acb7cf60147742acc985`  
		Last Modified: Fri, 09 Dec 2022 01:49:42 GMT  
		Size: 16.3 MB (16333067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc286146007ff4408affe775564aee13b831d6e988b8888027926639a7135bac`  
		Last Modified: Fri, 09 Dec 2022 01:51:07 GMT  
		Size: 198.5 MB (198463177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbd355f355665fbf881627666da7acd77bccd60f7d72faae5a3deb944eb07574`  
		Last Modified: Fri, 09 Dec 2022 01:50:53 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d200f814e9be8784c7653e788d0ba1013824e2f84c2297e2d4ab4e7260b57b`  
		Last Modified: Fri, 09 Dec 2022 08:27:24 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7853a6305507d0ec8fa032ee806059c6fd3d3ec8c6770b18ab1943aaeccd643`  
		Last Modified: Fri, 09 Dec 2022 08:27:35 GMT  
		Size: 65.3 MB (65307909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6488f753fa1649d49f9684bdf75dfcdb177eafaa8d5f1be405ada91a6a4eec25`  
		Last Modified: Fri, 09 Dec 2022 08:31:44 GMT  
		Size: 107.7 MB (107691695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk11-focal` - linux; arm variant v7

```console
$ docker pull gradle@sha256:d2bfea82a331a033fd36c1829332c65787ad27818d51786b6a8c20f06bd85dc4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **393.1 MB (393060769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9bb389c201a689732fef90dc6e2f7b95df514302289cc6c4cbfdcda801ae54f0`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 Dec 2022 01:36:16 GMT
ADD file:b21aa237ba47147762a1b92947251163795189df45212a32e07ea3438a186e03 in / 
# Fri, 09 Dec 2022 01:36:17 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:07:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:07:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:07:17 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:07:34 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 09 Dec 2022 03:09:10 GMT
ENV JAVA_VERSION=jdk-11.0.17+8
# Fri, 09 Dec 2022 03:09:27 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='d18b5dd73fce9edd5c58f623a1173f9ee2d45023836b8753b96beae51673a432';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.17_8.tar.gz';          ;;        armhf|arm)          ESUM='9ff3b4bd2bac18fb39f3356148efa2dc710ac029e12dc8f18ea1fe6be23bf299';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_arm_linux_hotspot_11.0.17_8.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='18c636bd103e240d29cdb30d7867720ea9fb9ff7c645738bfb4d5b8027269263';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.17_8.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='eb861db1433ddc1b89f170b789fafde282f137218d6d985fb5c2003e4ff44984';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.17_8.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='b8d46ed08ef4859476fe6421a7690d899ed83dce63f13fd894f994043177ef3c';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.17%2B8/OpenJDK11U-jdk_x64_linux_hotspot_11.0.17_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Fri, 09 Dec 2022 03:09:31 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Fri, 09 Dec 2022 03:09:31 GMT
CMD ["jshell"]
# Fri, 09 Dec 2022 05:49:59 GMT
CMD ["gradle"]
# Fri, 09 Dec 2022 05:49:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 09 Dec 2022 05:50:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Fri, 09 Dec 2022 05:50:00 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 09 Dec 2022 05:50:00 GMT
WORKDIR /home/gradle
# Fri, 09 Dec 2022 05:50:19 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Fri, 09 Dec 2022 05:54:01 GMT
ENV GRADLE_VERSION=6.9.3
# Fri, 09 Dec 2022 05:54:01 GMT
ARG GRADLE_DOWNLOAD_SHA256=dcf350b8ae1aa192fc299aed6efc77b43825d4fedb224c94118ae7faf5fb035d
# Fri, 09 Dec 2022 05:54:07 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=dcf350b8ae1aa192fc299aed6efc77b43825d4fedb224c94118ae7faf5fb035d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:cfbc8b467b3eb89e7c394402566b2965c83f3103dafb141203e0020a8acd3774`  
		Last Modified: Fri, 09 Dec 2022 01:38:40 GMT  
		Size: 24.6 MB (24589003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:164c34edcd59d52d7384160254a69600c5656e1c7173177cac362094db23b22a`  
		Last Modified: Fri, 09 Dec 2022 03:17:03 GMT  
		Size: 15.2 MB (15175201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:343a5f0e27d32f3ffd38559048de5b28ff2dc8b44a4fcb82b3a1de6dab5c5dfe`  
		Last Modified: Fri, 09 Dec 2022 03:18:45 GMT  
		Size: 185.9 MB (185891909 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10fe34d0df05bb9efc157622027d2352b7c8e8f7286319fc4c6b75cef42cf179`  
		Last Modified: Fri, 09 Dec 2022 03:18:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5eb4a3823267ece6a55a2c365942e75c7af93d6b09117303900e01c14f06f6b5`  
		Last Modified: Fri, 09 Dec 2022 06:01:53 GMT  
		Size: 4.3 KB (4321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e487507c7681787f7094eeae87c054bbdf23ce3084bd560f2e8100bd73554140`  
		Last Modified: Fri, 09 Dec 2022 06:01:56 GMT  
		Size: 59.7 MB (59708460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98a64a2bfbf8dc830f5b6e224ed6f44a565293b5098e01f6cb478f74990588b3`  
		Last Modified: Fri, 09 Dec 2022 06:07:32 GMT  
		Size: 107.7 MB (107691700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk11-focal` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:cb75c01e8e4bf39beefe919a6427df03c7790d783f209e9e61cd2b8bbd4d9d85
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **411.4 MB (411390132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe186f033509a5b7c85c7d8932fb548a108b58162dc244b4bc5dfe7e91e7fda`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 Dec 2022 01:46:50 GMT
ADD file:8cba976cb6ea226de769a768ee274e7679d34f923c93392f340680dc6696232e in / 
# Fri, 09 Dec 2022 01:46:50 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 03:38:47 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 03:38:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 03:38:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 03:39:07 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 17:41:01 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 24 Jan 2023 17:41:22 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 24 Jan 2023 17:41:25 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 24 Jan 2023 17:41:25 GMT
CMD ["jshell"]
# Tue, 24 Jan 2023 22:01:05 GMT
CMD ["gradle"]
# Tue, 24 Jan 2023 22:01:05 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 24 Jan 2023 22:01:05 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 24 Jan 2023 22:01:05 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 24 Jan 2023 22:01:06 GMT
WORKDIR /home/gradle
# Tue, 24 Jan 2023 22:01:49 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 24 Jan 2023 22:03:02 GMT
ENV GRADLE_VERSION=6.9.3
# Tue, 24 Jan 2023 22:03:02 GMT
ARG GRADLE_DOWNLOAD_SHA256=dcf350b8ae1aa192fc299aed6efc77b43825d4fedb224c94118ae7faf5fb035d
# Tue, 24 Jan 2023 22:03:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=dcf350b8ae1aa192fc299aed6efc77b43825d4fedb224c94118ae7faf5fb035d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:f04b4bbe15805316c8fda79beedd3b77e6b1ffcd0acf81226c3089e63f6bffeb`  
		Last Modified: Thu, 08 Dec 2022 15:28:02 GMT  
		Size: 27.2 MB (27193168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d371657879ab4e130d4ef0cad592b6a80196fce854ad341ab9641b484d81b17`  
		Last Modified: Fri, 09 Dec 2022 03:45:13 GMT  
		Size: 16.2 MB (16202837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca5932f95e7e5936ca29b485d000a60428e9c176f053cb6e575ee7b68601cfbf`  
		Last Modified: Tue, 24 Jan 2023 17:46:30 GMT  
		Size: 195.2 MB (195247167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9dcf884b63c29a81e30ef46ebb32a59539752951febce6ba3efd58e0e1d0bbc`  
		Last Modified: Tue, 24 Jan 2023 17:46:19 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bc7f68e2817578f0e1af12559ca4c56634f377f51f57ecc9772595006189a06`  
		Last Modified: Tue, 24 Jan 2023 22:05:39 GMT  
		Size: 4.4 KB (4369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e846d9e709a97a03a9a59a9306340dead638d8e92ef21448350686b53eec0958`  
		Last Modified: Tue, 24 Jan 2023 22:05:48 GMT  
		Size: 65.1 MB (65050725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cda3b1a630f675064076abeb08035078e5e4fc10fecc2803280fba6c42f52c39`  
		Last Modified: Tue, 24 Jan 2023 22:08:17 GMT  
		Size: 107.7 MB (107691691 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk11-focal` - linux; ppc64le

```console
$ docker pull gradle@sha256:b5e80e0490352718d4b0a14617e953773f2ea4734fe6d07425348e28eccc7936
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **412.8 MB (412767720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ac9f472ee00fd7a69feddc39deac2ebaa7a89af8b35a53b2254f0f8ac34a17`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 Dec 2022 01:27:36 GMT
ADD file:ca32a106475146fa5bd0f3e4920ea64671b1054f57a1f33d4681fe170deda313 in / 
# Fri, 09 Dec 2022 01:27:37 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:38:43 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:38:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:38:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:39:10 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 18:17:30 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 24 Jan 2023 18:17:51 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 24 Jan 2023 18:17:58 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 24 Jan 2023 18:17:58 GMT
CMD ["jshell"]
# Tue, 24 Jan 2023 21:35:19 GMT
CMD ["gradle"]
# Tue, 24 Jan 2023 21:35:19 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 24 Jan 2023 21:35:21 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 24 Jan 2023 21:35:21 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 24 Jan 2023 21:35:21 GMT
WORKDIR /home/gradle
# Tue, 24 Jan 2023 21:36:28 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 24 Jan 2023 21:39:42 GMT
ENV GRADLE_VERSION=6.9.3
# Tue, 24 Jan 2023 21:39:43 GMT
ARG GRADLE_DOWNLOAD_SHA256=dcf350b8ae1aa192fc299aed6efc77b43825d4fedb224c94118ae7faf5fb035d
# Tue, 24 Jan 2023 21:39:52 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=dcf350b8ae1aa192fc299aed6efc77b43825d4fedb224c94118ae7faf5fb035d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:d198f08d15a240101119086908bf4c5035dc657d52bfe206ddeede273c6b84f3`  
		Last Modified: Fri, 09 Dec 2022 01:30:09 GMT  
		Size: 33.3 MB (33299473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34311a239abf8081ab4c6a2e290ba93bc7ff41b6729bbc85d7cb2c321f7e3c33`  
		Last Modified: Fri, 09 Dec 2022 02:52:31 GMT  
		Size: 17.6 MB (17571798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abebc0ed0f76ac9360c307e27675be1c545dbf6fc553241c38ffdebd3d1bb88b`  
		Last Modified: Tue, 24 Jan 2023 18:28:19 GMT  
		Size: 180.5 MB (180465927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a15eb85715bfd03a31e7802713cd52ee056625f983c5f337bb69f7c319eaf366`  
		Last Modified: Tue, 24 Jan 2023 18:27:56 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:802b1cda58ed66960b06dc43d5f98988f33f8e8605dc181f16958f149fe8be39`  
		Last Modified: Tue, 24 Jan 2023 21:45:12 GMT  
		Size: 4.4 KB (4359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aedb2eba283f4546c8c5d352af805d65583d6d6737e9257b532cb415fda59d3`  
		Last Modified: Tue, 24 Jan 2023 21:45:33 GMT  
		Size: 73.7 MB (73734327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59895c340c04fe0bc8020685662d39e88cf0f42d49a57438cf888142582eaafc`  
		Last Modified: Tue, 24 Jan 2023 21:49:28 GMT  
		Size: 107.7 MB (107691661 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk11-focal` - linux; s390x

```console
$ docker pull gradle@sha256:840366ededb20d4ca20b413648ceb5b9b05ec746d6b44c087c8913ffd40da23a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **387.2 MB (387213248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd8b79eda5b60da5a67f33a56d9310fb782b2032b9dc288c75e718413a40b40`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 09 Dec 2022 01:52:40 GMT
ADD file:3d26982d2188d52ed2423587d3d2597c1f8ff614c19408d892cadc91d3743deb in / 
# Fri, 09 Dec 2022 01:52:43 GMT
CMD ["bash"]
# Fri, 09 Dec 2022 02:11:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 09 Dec 2022 02:11:30 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 09 Dec 2022 02:11:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 09 Dec 2022 02:12:20 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 24 Jan 2023 17:41:55 GMT
ENV JAVA_VERSION=jdk-11.0.18+10
# Tue, 24 Jan 2023 17:42:03 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='04d5eeff6a6449bcdca0f52cd97bafd43ce09d40ef1e73fa0e1add63bea4a9c8';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_aarch64_linux_hotspot_11.0.18_10.tar.gz';          ;;        armhf|arm)          ESUM='b42840ef88621f87a4b49ae3a8db23dbf07cd9e7fb62823318709a592f597ea3';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_arm_linux_hotspot_11.0.18_10.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='459148d489b08ceec2d901e950ac36722b4c55e907e979291ddfc954ebdcea47';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_ppc64le_linux_hotspot_11.0.18_10.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='7a7193c8279dd889c0a39296bcbae8866d94cff7a6d1bdfe676ffe4ced018915';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_s390x_linux_hotspot_11.0.18_10.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='4a29efda1d702b8ff38e554cf932051f40ec70006caed5c4857a8cbc7a0b7db7';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.18%2B10/OpenJDK11U-jdk_x64_linux_hotspot_11.0.18_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/src.zip;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Tue, 24 Jan 2023 17:42:08 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Tue, 24 Jan 2023 17:42:08 GMT
CMD ["jshell"]
# Tue, 24 Jan 2023 19:55:41 GMT
CMD ["gradle"]
# Tue, 24 Jan 2023 19:55:41 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 24 Jan 2023 19:55:42 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln --symbolic /home/gradle/.gradle /root/.gradle
# Tue, 24 Jan 2023 19:55:42 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 24 Jan 2023 19:55:42 GMT
WORKDIR /home/gradle
# Tue, 24 Jan 2023 19:56:22 GMT
RUN set -o errexit -o nounset     && apt-get update     && apt-get install --yes --no-install-recommends         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm --recursive --force /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Tue, 24 Jan 2023 19:58:10 GMT
ENV GRADLE_VERSION=6.9.3
# Tue, 24 Jan 2023 19:58:10 GMT
ARG GRADLE_DOWNLOAD_SHA256=dcf350b8ae1aa192fc299aed6efc77b43825d4fedb224c94118ae7faf5fb035d
# Tue, 24 Jan 2023 19:58:15 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=dcf350b8ae1aa192fc299aed6efc77b43825d4fedb224c94118ae7faf5fb035d
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:5d330d9ae4f68425a719ebb93a3911994ee56b1328cf256fc3c44a4050de22ec`  
		Last Modified: Fri, 09 Dec 2022 01:54:57 GMT  
		Size: 27.0 MB (27016083 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02a678a3aa5292081c0c30d5d64b1cc8a8b017331407ba4f52d381d8700e78f7`  
		Last Modified: Fri, 09 Dec 2022 02:23:39 GMT  
		Size: 16.0 MB (16037979 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3411b3f29f8b48271e05510f62ced2f0d44517b1a5ac6012a8e69ec3e80dce`  
		Last Modified: Tue, 24 Jan 2023 17:47:35 GMT  
		Size: 172.0 MB (171957857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b869f5860ae7b18cae911c9543845321ca099bda7a5c1c081df73718c4b80b05`  
		Last Modified: Tue, 24 Jan 2023 17:47:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60d25348b9a9eb032158a2f2bedbb49f298c15720d756e01d6e15075dab8b52e`  
		Last Modified: Tue, 24 Jan 2023 20:02:07 GMT  
		Size: 4.4 KB (4364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11d02bbcb4d55bd36928b4dda43c54c9406889871f7acf7f17688b7eb62d3c3a`  
		Last Modified: Tue, 24 Jan 2023 20:02:17 GMT  
		Size: 64.5 MB (64505086 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2ecc036b6ca14bda96015a24264a6f50cc755b7eae937dba44dfef144e7bd32`  
		Last Modified: Tue, 24 Jan 2023 20:04:34 GMT  
		Size: 107.7 MB (107691705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
