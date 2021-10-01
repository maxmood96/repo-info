## `gradle:jre16`

```console
$ docker pull gradle@sha256:0d926de17242c1defdf55dd485f060693803b2deb2feafd5c534c434c5afbf33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:jre16` - linux; amd64

```console
$ docker pull gradle@sha256:e91490d05c3f516cd52c4bf18730cea45fccf252aeae572f9d3159bcd110b16f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.2 MB (274229146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c5e64eeb90731ffab5b0b90d90ca83b80d40ffbf4801ea28618ec3f00ea0d27`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 31 Aug 2021 01:20:55 GMT
ADD file:d2abf27fe2e8b0b5f4da68c018560c73e11c53098329246e3e6fe176698ef941 in / 
# Tue, 31 Aug 2021 01:20:56 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:26:05 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:26:55 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:28:03 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Tue, 31 Aug 2021 02:28:24 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4e47f1cbf46190727be74cd73445ec2b693f5ba4a74542c554d6b3285811cab5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='c1f88f3ce955cb2e9a4236a916cc6660ef55231d29c4390b1a4398ebbca358b7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='495805e2e9bcabeac0d8271623b6c92604440608286f4ce411ea48f582854930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='780f10923df3230b6013c74482adcc6d8c1fef7b60aefe59a0b337183767d214';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5eca19d406c6d130e9c3a4b932b9cb0a6e9cd45932450668c3e911bded4bcf40';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:28:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 07:09:11 GMT
CMD ["gradle"]
# Tue, 31 Aug 2021 07:09:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Aug 2021 07:09:12 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 31 Aug 2021 07:09:12 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Aug 2021 07:09:12 GMT
WORKDIR /home/gradle
# Tue, 31 Aug 2021 07:09:31 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 07:09:32 GMT
ENV GRADLE_VERSION=7.2
# Tue, 31 Aug 2021 07:09:32 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Tue, 31 Aug 2021 07:09:37 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:35807b77a593c1147d13dc926a91dcc3015616ff7307cc30442c5a8e07546283`  
		Last Modified: Sat, 28 Aug 2021 03:03:19 GMT  
		Size: 28.6 MB (28570074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93d71b8f96bb4f1c00b7375be1090b56f03343a56b15fdcdf40d5ac4a207e217`  
		Last Modified: Tue, 31 Aug 2021 02:37:06 GMT  
		Size: 16.0 MB (16033698 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9058bc26dd87a5dc0a7fb4a814b3c2b96b80f8ac56863c0d1a61c9244a84a04c`  
		Last Modified: Tue, 31 Aug 2021 02:39:59 GMT  
		Size: 49.6 MB (49621492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b597ac16d00d1be7a67eec7b55acec676924ebda4e1c48c0f4056c32d3c5a2b`  
		Last Modified: Tue, 31 Aug 2021 07:20:53 GMT  
		Size: 4.4 KB (4359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94515159830456d41cf25d30844ff197d629963997de581bef16a6f0c4a88585`  
		Last Modified: Tue, 31 Aug 2021 07:21:04 GMT  
		Size: 65.6 MB (65625675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:151476888f9e465bfb7302d141a42f7e4a3bc0490130ac32b87d28db199ff701`  
		Last Modified: Tue, 31 Aug 2021 07:21:03 GMT  
		Size: 114.4 MB (114373848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre16` - linux; arm variant v7

```console
$ docker pull gradle@sha256:118229f5b5ab660c86e4b42ccf9666a19515cf1853315fafab7beb3bca6416b7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.0 MB (258036708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5c5cb4bccadede4746a5f0378baa301bcdae5ba13b585c8b8e88e9e218e68ba`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 31 Aug 2021 01:40:52 GMT
ADD file:f9dcf17ef0f45719dff5ed961907d78a1ea6671fecdb434536f3fc8cf15fbb3b in / 
# Tue, 31 Aug 2021 01:40:53 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:51:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:52:01 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:55:27 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Tue, 31 Aug 2021 02:56:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4e47f1cbf46190727be74cd73445ec2b693f5ba4a74542c554d6b3285811cab5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='c1f88f3ce955cb2e9a4236a916cc6660ef55231d29c4390b1a4398ebbca358b7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='495805e2e9bcabeac0d8271623b6c92604440608286f4ce411ea48f582854930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='780f10923df3230b6013c74482adcc6d8c1fef7b60aefe59a0b337183767d214';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5eca19d406c6d130e9c3a4b932b9cb0a6e9cd45932450668c3e911bded4bcf40';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:56:26 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 05:28:21 GMT
CMD ["gradle"]
# Tue, 31 Aug 2021 05:28:22 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Aug 2021 05:28:23 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 31 Aug 2021 05:28:24 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Aug 2021 05:28:24 GMT
WORKDIR /home/gradle
# Tue, 31 Aug 2021 05:29:13 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 05:29:14 GMT
ENV GRADLE_VERSION=7.2
# Tue, 31 Aug 2021 05:29:15 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Tue, 31 Aug 2021 05:29:27 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:cccc98128e2b3db00394b4e59c3f674a52e4b861786d9fab388357a88fc428a2`  
		Last Modified: Tue, 31 Aug 2021 01:44:57 GMT  
		Size: 24.1 MB (24068823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b915f774c910de28b940b41c37fc76946eb150ac0a4048d2d2cbc5b3b0983c26`  
		Last Modified: Tue, 31 Aug 2021 02:59:59 GMT  
		Size: 14.9 MB (14902564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7171b909b5daf250c6239000693d9545bac063480cebac810dba441593704e00`  
		Last Modified: Tue, 31 Aug 2021 03:07:48 GMT  
		Size: 44.7 MB (44663213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5eb122176bee317198e0f1105724815334f5e2abbf2a88790c31b4d1c1a175f`  
		Last Modified: Tue, 31 Aug 2021 05:39:07 GMT  
		Size: 4.3 KB (4345 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35761802863366d4a94b489bdd4cb96f1f392cd0f5b87cf97fa057d6204791d`  
		Last Modified: Tue, 31 Aug 2021 05:39:50 GMT  
		Size: 60.0 MB (60023894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6949523b012287774b5b09a87ef0c754f32c7b2fed504fb03796a6c85d8b79e4`  
		Last Modified: Tue, 31 Aug 2021 05:39:39 GMT  
		Size: 114.4 MB (114373869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre16` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:046380fc97f9743869f5455ef20e05d882feabbead49c7eed9d45434618684ee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.2 MB (271197233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4e23ac1a91b00ab650210811cc5be5c32db66298a5ce4befc491afd5c84e215`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:02:25 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:03:48 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Fri, 01 Oct 2021 03:04:14 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4e47f1cbf46190727be74cd73445ec2b693f5ba4a74542c554d6b3285811cab5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='c1f88f3ce955cb2e9a4236a916cc6660ef55231d29c4390b1a4398ebbca358b7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='495805e2e9bcabeac0d8271623b6c92604440608286f4ce411ea48f582854930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='780f10923df3230b6013c74482adcc6d8c1fef7b60aefe59a0b337183767d214';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5eca19d406c6d130e9c3a4b932b9cb0a6e9cd45932450668c3e911bded4bcf40';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:04:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:31:08 GMT
CMD ["gradle"]
# Fri, 01 Oct 2021 04:31:08 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 01 Oct 2021 04:31:09 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 01 Oct 2021 04:31:09 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 01 Oct 2021 04:31:10 GMT
WORKDIR /home/gradle
# Fri, 01 Oct 2021 04:31:30 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:31:31 GMT
ENV GRADLE_VERSION=7.2
# Fri, 01 Oct 2021 04:31:31 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Fri, 01 Oct 2021 04:31:36 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965f9c84d32763760a8a95b798239bf2dd8423aeb8fb56015ddd90196d483d9f`  
		Last Modified: Fri, 01 Oct 2021 03:06:06 GMT  
		Size: 15.9 MB (15895939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22d94c05262d780295dd8214b29db520cbaead56c618f3bf2531dbb268af5d84`  
		Last Modified: Fri, 01 Oct 2021 03:09:11 GMT  
		Size: 48.4 MB (48422624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4753c953c011b0b265e3580968df83351d969655a76f2b6ce936880412740697`  
		Last Modified: Fri, 01 Oct 2021 04:44:16 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e872bd19233a58831135ef5cec3e22c473cbf4bbd0bd7d5a9646975c7219323d`  
		Last Modified: Fri, 01 Oct 2021 04:44:28 GMT  
		Size: 65.3 MB (65328130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed1db0756b51b4e2053b8ab7928375a457b77147033cf677aa68633a6ffe2d71`  
		Last Modified: Fri, 01 Oct 2021 04:44:24 GMT  
		Size: 114.4 MB (114373770 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre16` - linux; ppc64le

```console
$ docker pull gradle@sha256:0f8e2f7973a6b7438de2b20d7c3b811983c6830ac3a1ad282396d231c017c5d6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **283.7 MB (283735323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bb64edc8a279e02472778717166d7f16a8f0f8e1df4fad3ef1243fac4dc76bb`
-	Default Command: `["gradle"]`

```dockerfile
# Tue, 31 Aug 2021 02:10:40 GMT
ADD file:7e5ee5560faaa801aa10a76122190026f8c1da00c809f4fb6ff441751ba0c90f in / 
# Tue, 31 Aug 2021 02:10:45 GMT
CMD ["bash"]
# Tue, 31 Aug 2021 02:31:18 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 31 Aug 2021 02:33:24 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 02:37:45 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Tue, 31 Aug 2021 02:39:04 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4e47f1cbf46190727be74cd73445ec2b693f5ba4a74542c554d6b3285811cab5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='c1f88f3ce955cb2e9a4236a916cc6660ef55231d29c4390b1a4398ebbca358b7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='495805e2e9bcabeac0d8271623b6c92604440608286f4ce411ea48f582854930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='780f10923df3230b6013c74482adcc6d8c1fef7b60aefe59a0b337183767d214';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5eca19d406c6d130e9c3a4b932b9cb0a6e9cd45932450668c3e911bded4bcf40';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:39:11 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 07:56:07 GMT
CMD ["gradle"]
# Tue, 31 Aug 2021 07:56:14 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Aug 2021 07:56:27 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 31 Aug 2021 07:56:30 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Aug 2021 07:56:36 GMT
WORKDIR /home/gradle
# Tue, 31 Aug 2021 08:02:22 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 08:02:28 GMT
ENV GRADLE_VERSION=7.2
# Tue, 31 Aug 2021 08:02:35 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Tue, 31 Aug 2021 08:03:00 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:59390c695558464c51dc1fced64934b549770630192a1639ac6a90f59bd63b13`  
		Last Modified: Tue, 31 Aug 2021 02:14:21 GMT  
		Size: 33.3 MB (33291791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df6df1a3e21a26bf9e0775ad823e1762b00bf8c2a0650a891b7860b7fe18741a`  
		Last Modified: Tue, 31 Aug 2021 02:54:54 GMT  
		Size: 17.2 MB (17208636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b6914bc910b228b8ef6d99dfdb4ea1b290b8e76ece716b73ebd8a67fda256d4`  
		Last Modified: Tue, 31 Aug 2021 02:58:15 GMT  
		Size: 44.9 MB (44852180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d48535f41deeaa2a15d7606849773ec588758edb81f7ea11035f6bed5a895554`  
		Last Modified: Tue, 31 Aug 2021 09:04:01 GMT  
		Size: 4.4 KB (4361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e556d0dd61a1a01c124ea0be784ecb6a50ddfda7b06ccfcb2b5159a2d77b352b`  
		Last Modified: Tue, 31 Aug 2021 09:05:12 GMT  
		Size: 74.0 MB (74004485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3e8746551fe1c7668d4ccc1453f8cbefacc3398e276e89670fc540873b66f07`  
		Last Modified: Tue, 31 Aug 2021 09:04:23 GMT  
		Size: 114.4 MB (114373870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:jre16` - linux; s390x

```console
$ docker pull gradle@sha256:d9c4f1a468df0ff36c6c3d11eb277b43a337b5bf5f8f82d00dd781d483a19ee2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **266.1 MB (266112210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:731073c8520549ca22f1595c6571f61f7cbba5457ee3b668fce403b72ceea1e6`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Oct 2021 01:42:28 GMT
ADD file:28b3d1959812d7666f9f73b52562cdaaaf84ff25ce6331995e21c66bb31b0cc2 in / 
# Fri, 01 Oct 2021 01:42:30 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 02:00:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 02:00:17 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 02:01:57 GMT
ENV JAVA_VERSION=jdk-16.0.1+9
# Fri, 01 Oct 2021 02:02:26 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='4e47f1cbf46190727be74cd73445ec2b693f5ba4a74542c554d6b3285811cab5';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_aarch64_linux_hotspot_16.0.1_9.tar.gz';          ;;        armhf|armv7l)          ESUM='c1f88f3ce955cb2e9a4236a916cc6660ef55231d29c4390b1a4398ebbca358b7';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_arm_linux_hotspot_16.0.1_9.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='495805e2e9bcabeac0d8271623b6c92604440608286f4ce411ea48f582854930';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_ppc64le_linux_hotspot_16.0.1_9.tar.gz';          ;;        s390x)          ESUM='780f10923df3230b6013c74482adcc6d8c1fef7b60aefe59a0b337183767d214';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_s390x_linux_hotspot_16.0.1_9.tar.gz';          ;;        amd64|x86_64)          ESUM='5eca19d406c6d130e9c3a4b932b9cb0a6e9cd45932450668c3e911bded4bcf40';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk16-binaries/releases/download/jdk-16.0.1%2B9/OpenJDK16U-jre_x64_linux_hotspot_16.0.1_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 02:02:27 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 02:52:25 GMT
CMD ["gradle"]
# Fri, 01 Oct 2021 02:52:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 01 Oct 2021 02:52:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 01 Oct 2021 02:52:26 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 01 Oct 2021 02:52:26 GMT
WORKDIR /home/gradle
# Fri, 01 Oct 2021 02:52:42 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 02:52:45 GMT
ENV GRADLE_VERSION=7.2
# Fri, 01 Oct 2021 02:52:46 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Fri, 01 Oct 2021 02:52:51 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:21245da3aae0a4172d9a415c8ba92069601c8a55fc39b783bce7981e97de1b4d`  
		Last Modified: Fri, 01 Oct 2021 01:44:02 GMT  
		Size: 27.1 MB (27122910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1b23a8bdcc3c25fc238593c281d2480b42fe86d322be5a1580ea62c30b309a9`  
		Last Modified: Fri, 01 Oct 2021 02:12:12 GMT  
		Size: 15.7 MB (15739781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38ca3efaae54312e26c738e57017707c109b255caececf6c3c06fe66cc117eb`  
		Last Modified: Fri, 01 Oct 2021 02:14:13 GMT  
		Size: 44.0 MB (44034537 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b706c181d7bb0f75b5559ec5f979c5f17b184a2378097736df6c4316983a54c`  
		Last Modified: Fri, 01 Oct 2021 03:07:11 GMT  
		Size: 4.4 KB (4365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f32eca31abd99927f3585fea57628a542822f2b6b793d22088edd1a6ee051d99`  
		Last Modified: Fri, 01 Oct 2021 03:07:21 GMT  
		Size: 64.8 MB (64836773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ac7464fa95c468007e4a8426cd9d1c9e95256f7e5c3a392d04bd5e5eacdc88`  
		Last Modified: Fri, 01 Oct 2021 03:07:16 GMT  
		Size: 114.4 MB (114373844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
