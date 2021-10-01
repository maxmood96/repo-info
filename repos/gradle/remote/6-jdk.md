## `gradle:6-jdk`

```console
$ docker pull gradle@sha256:c0ab1b8d011fda54c0599929ae27f1485f242ee550f0aa370dae730647d5385b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; ppc64le
	-	linux; s390x

### `gradle:6-jdk` - linux; amd64

```console
$ docker pull gradle@sha256:2320e7461f6f99c04bf91daa9747c812a7891e749706163f2a89e6a14d8af289
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.5 MB (321475694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b721da90ca395b8b7d2aba137c6a9c772a81c60157c470cde6569ca071307f67`
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
# Tue, 31 Aug 2021 02:26:55 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Tue, 31 Aug 2021 02:27:01 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a29edaf66221f7a51353d3f28e1ecf4221268848260417bc562d797e514082a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='0de107b7df38314c1daab78571383b8b39fdc506790aaef5d870b3e70048881b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ecf00e57033296fd23201477a64dc13a1356b16a635907e104d079ddb544e4b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='276a431c79b7e94bc1b1b4fd88523383ae2d635ea67114dfc8a6174267f8fb2c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='0949505fcf42a1765558048451bb2a22e84b3635b1a31dd6191780eeccaa4ada';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:27:01 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 07:06:09 GMT
CMD ["gradle"]
# Tue, 31 Aug 2021 07:06:09 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Aug 2021 07:06:10 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 31 Aug 2021 07:06:10 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Aug 2021 07:06:10 GMT
WORKDIR /home/gradle
# Tue, 31 Aug 2021 07:06:51 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 07:12:42 GMT
ENV GRADLE_VERSION=6.9.1
# Tue, 31 Aug 2021 07:12:42 GMT
ARG GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
# Tue, 31 Aug 2021 07:12:47 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
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
	-	`sha256:eec3d23cb0f5b8bb10ed969c7b1d003896ec72a3a34bfb13cd43a9f395f8e747`  
		Last Modified: Tue, 31 Aug 2021 02:37:13 GMT  
		Size: 103.6 MB (103551844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc785331fab30a46c61c03ea4dedf41b3fccdcf9b4fc5cfe060d2c3edd4290cf`  
		Last Modified: Tue, 31 Aug 2021 07:16:29 GMT  
		Size: 4.4 KB (4362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817a59667772e7dff2ee35d41767d3c67e43377c0dcb754d9b195c548289280c`  
		Last Modified: Tue, 31 Aug 2021 07:16:42 GMT  
		Size: 65.6 MB (65625833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce8b2803aa6fbd087204bd7b7b826b96768d9e32083fb99bf2603e6119cce55`  
		Last Modified: Tue, 31 Aug 2021 07:25:01 GMT  
		Size: 107.7 MB (107689883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:242a60cda036088e2a52e5e89b9196a1390605adb02349c63dc5615b96f72e5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **319.0 MB (319046847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992ae2a3030a9842bdc5506ae734bdcd277a894158a7c73e385f4ac0c4b74b2a`
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
# Fri, 01 Oct 2021 03:02:25 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Fri, 01 Oct 2021 03:02:31 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a29edaf66221f7a51353d3f28e1ecf4221268848260417bc562d797e514082a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='0de107b7df38314c1daab78571383b8b39fdc506790aaef5d870b3e70048881b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ecf00e57033296fd23201477a64dc13a1356b16a635907e104d079ddb544e4b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='276a431c79b7e94bc1b1b4fd88523383ae2d635ea67114dfc8a6174267f8fb2c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='0949505fcf42a1765558048451bb2a22e84b3635b1a31dd6191780eeccaa4ada';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 03:02:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 04:27:59 GMT
CMD ["gradle"]
# Fri, 01 Oct 2021 04:27:59 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 01 Oct 2021 04:28:00 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 01 Oct 2021 04:28:00 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 01 Oct 2021 04:28:00 GMT
WORKDIR /home/gradle
# Fri, 01 Oct 2021 04:28:20 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 04:32:24 GMT
ENV GRADLE_VERSION=6.9.1
# Fri, 01 Oct 2021 04:32:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
# Fri, 01 Oct 2021 04:32:28 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
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
	-	`sha256:132be1dc4dbe9d7d252158df0a96c5b7e6f78c83e602eb47878efdb4e55db2f2`  
		Last Modified: Fri, 01 Oct 2021 03:06:14 GMT  
		Size: 103.0 MB (102955969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bce6036010968d3499d76011d9e32d816d308cde7a9086cd61a3e778c0c8f572`  
		Last Modified: Fri, 01 Oct 2021 04:39:16 GMT  
		Size: 4.4 KB (4367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adeb6005fec38d705896efb760bc23a8ded68e7864b462cad4dc06648ec26036`  
		Last Modified: Fri, 01 Oct 2021 04:39:29 GMT  
		Size: 65.3 MB (65328291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8f35641675511bac4d9a30d0e0bbf858290bf1eb667e65b30bbc533677f3c8a`  
		Last Modified: Fri, 01 Oct 2021 04:45:34 GMT  
		Size: 107.7 MB (107689876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk` - linux; ppc64le

```console
$ docker pull gradle@sha256:9ab407e3e7e6dd0141a7c868fcbbfe994b19ac38e7a6ed18ad0295d2173d2d81
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **333.2 MB (333247127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8ba6bb130fb9889e62169dac8b18748a45d1878e1cc07a85dcf4f459a184ca6`
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
# Tue, 31 Aug 2021 02:33:30 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Tue, 31 Aug 2021 02:33:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a29edaf66221f7a51353d3f28e1ecf4221268848260417bc562d797e514082a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='0de107b7df38314c1daab78571383b8b39fdc506790aaef5d870b3e70048881b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ecf00e57033296fd23201477a64dc13a1356b16a635907e104d079ddb544e4b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='276a431c79b7e94bc1b1b4fd88523383ae2d635ea67114dfc8a6174267f8fb2c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='0949505fcf42a1765558048451bb2a22e84b3635b1a31dd6191780eeccaa4ada';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 31 Aug 2021 02:34:02 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Aug 2021 07:25:19 GMT
CMD ["gradle"]
# Tue, 31 Aug 2021 07:25:23 GMT
ENV GRADLE_HOME=/opt/gradle
# Tue, 31 Aug 2021 07:25:47 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Tue, 31 Aug 2021 07:25:52 GMT
VOLUME [/home/gradle/.gradle]
# Tue, 31 Aug 2021 07:25:57 GMT
WORKDIR /home/gradle
# Tue, 31 Aug 2021 07:30:41 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Tue, 31 Aug 2021 08:39:18 GMT
ENV GRADLE_VERSION=6.9.1
# Tue, 31 Aug 2021 08:39:24 GMT
ARG GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
# Tue, 31 Aug 2021 08:39:42 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
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
	-	`sha256:5d90bb7de86986840c8d8f475753fd83d18a1dca6b58eb19ed2f020231f1f24b`  
		Last Modified: Tue, 31 Aug 2021 02:55:01 GMT  
		Size: 101.0 MB (101047826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bacc7a30580a223680ef4e9174f15a60d9b19e239478de2bad23135b257490be`  
		Last Modified: Tue, 31 Aug 2021 08:52:45 GMT  
		Size: 4.4 KB (4369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17c2f93bfeffaef7c7de1f3c534423b027f4bd0f3db28c2c11c595bce692c64`  
		Last Modified: Tue, 31 Aug 2021 08:54:05 GMT  
		Size: 74.0 MB (74004598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026894e33a05cda6bee00bdb8982540c591d8af66b094812cdf253d893fb7e42`  
		Last Modified: Tue, 31 Aug 2021 09:19:19 GMT  
		Size: 107.7 MB (107689907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:6-jdk` - linux; s390x

```console
$ docker pull gradle@sha256:eb71d1889deb6ddaaee48a9ba54d62b9d4293a64b3be306b04101ae76660e946
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **314.0 MB (314032901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:040bf66f495f19e42a2a0e5cffef5d65688704ac2da1c75a97416542ec2cd68d`
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
# Fri, 01 Oct 2021 02:00:18 GMT
ENV JAVA_VERSION=jdk8u292-b10
# Fri, 01 Oct 2021 02:00:25 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='a29edaf66221f7a51353d3f28e1ecf4221268848260417bc562d797e514082a8';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_aarch64_linux_hotspot_8u292b10.tar.gz';          ;;        armhf|armv7l)          ESUM='0de107b7df38314c1daab78571383b8b39fdc506790aaef5d870b3e70048881b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_arm_linux_hotspot_8u292b10.tar.gz';          ;;        ppc64el|ppc64le)          ESUM='7ecf00e57033296fd23201477a64dc13a1356b16a635907e104d079ddb544e4b';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u292b10.tar.gz';          ;;        s390x)          ESUM='276a431c79b7e94bc1b1b4fd88523383ae2d635ea67114dfc8a6174267f8fb2c';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_s390x_linux_hotspot_8u292b10.tar.gz';          LIBFFI_SUM='05e456a2e8ad9f20db846ccb96c483235c3243e27025c3e8e8e358411fd48be9';          LIBFFI_URL='http://launchpadlibrarian.net/354371408/libffi6_3.2.1-8_s390x.deb';          curl -LfsSo /tmp/libffi6.deb ${LIBFFI_URL};          echo "${LIBFFI_SUM} /tmp/libffi6.deb" | sha256sum -c -;          apt-get install -y --no-install-recommends /tmp/libffi6.deb;          rm -rf /tmp/libffi6.deb;          ;;        amd64|x86_64)          ESUM='0949505fcf42a1765558048451bb2a22e84b3635b1a31dd6191780eeccaa4ada';          BINARY_URL='https://github.com/AdoptOpenJDK/openjdk8-binaries/releases/download/jdk8u292-b10/OpenJDK8U-jdk_x64_linux_hotspot_8u292b10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Fri, 01 Oct 2021 02:00:28 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 01 Oct 2021 02:49:15 GMT
CMD ["gradle"]
# Fri, 01 Oct 2021 02:49:15 GMT
ENV GRADLE_HOME=/opt/gradle
# Fri, 01 Oct 2021 02:49:16 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Fri, 01 Oct 2021 02:49:16 GMT
VOLUME [/home/gradle/.gradle]
# Fri, 01 Oct 2021 02:49:16 GMT
WORKDIR /home/gradle
# Fri, 01 Oct 2021 02:49:32 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 02:56:35 GMT
ENV GRADLE_VERSION=6.9.1
# Fri, 01 Oct 2021 02:56:36 GMT
ARG GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
# Fri, 01 Oct 2021 02:56:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=8c12154228a502b784f451179846e518733cf856efc7d45b2e6691012977b2fe
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
	-	`sha256:c2aa7dabcd217b41bae4f9e7b0c0c5e5254490f947726606896769cb25e7acd4`  
		Last Modified: Fri, 01 Oct 2021 02:12:17 GMT  
		Size: 98.6 MB (98640896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc3cb4871d5bdf53a5a82e00c01ccb98dc215ad3b94f45bbf1ea6947cf7a90b2`  
		Last Modified: Fri, 01 Oct 2021 03:03:56 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca746c7dbbcdc277cd4c5205705d3e9a44da11e1416a2ac67af7c0396630fe2`  
		Last Modified: Fri, 01 Oct 2021 03:04:06 GMT  
		Size: 64.8 MB (64835069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bb6b84b5b1ed3fb6666ff74ba5946c126737c34fd55e8d364660821d008d31`  
		Last Modified: Fri, 01 Oct 2021 03:10:14 GMT  
		Size: 107.7 MB (107689879 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
