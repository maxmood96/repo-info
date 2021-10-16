## `gradle:7-jdk8`

```console
$ docker pull gradle@sha256:b7cebf930884f526332a3d07ec28fbbf89a230e3cde59336ee6977c611dd0b6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `gradle:7-jdk8` - linux; amd64

```console
$ docker pull gradle@sha256:a2c4b3e64baa0dea72bdb2d9c9ee9ec38f91d6ad3dadb1efd73d6de8519c970e
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **328.2 MB (328157452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179105388dece3aa235f4bbed81d68322d8de1d17246564e24cfdc45c1e08a38`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 16 Oct 2021 00:37:47 GMT
ADD file:5d68d27cc15a80653c93d3a0b262a28112d47a46326ff5fc2dfbf7fa3b9a0ce8 in / 
# Sat, 16 Oct 2021 00:37:47 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:44:06 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:44:32 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:44:32 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Sat, 16 Oct 2021 02:44:38 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f287cdc2a688c2df247ea0d8bfe2863645b73848e4e5c35b02a8a3d2d6b69551';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        armhf|arm)          ESUM='666f159ab0a2dd09c776681eb7cecaf04dc17e35deb213e588fe4f00c2fcac24';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u302b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='c2940f3772d4467a818a0221e80c2c720b6d427a886aaed37262e451ddbb0a56';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='cc13f274becf9dd5517b6be583632819dfd4dd81e524b5c1b4f406bdaf0e063a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 02:44:39 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 02:44:40 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 16 Oct 2021 04:40:25 GMT
CMD ["gradle"]
# Sat, 16 Oct 2021 04:40:25 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 16 Oct 2021 04:40:26 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 16 Oct 2021 04:40:27 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 16 Oct 2021 04:40:27 GMT
WORKDIR /home/gradle
# Sat, 16 Oct 2021 04:40:59 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 16 Oct 2021 04:41:00 GMT
ENV GRADLE_VERSION=7.2
# Sat, 16 Oct 2021 04:41:00 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Sat, 16 Oct 2021 04:41:05 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:7b1a6ab2e44dbac178598dabe7cff59bd67233dba0b27e4fbd1f9d4b3c877a54`  
		Last Modified: Thu, 07 Oct 2021 23:44:23 GMT  
		Size: 28.6 MB (28567101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237daeb1ae282fe20092079ef6d5de7924746d0f2e9ad88797d08524a4d842fd`  
		Last Modified: Sat, 16 Oct 2021 02:47:20 GMT  
		Size: 16.0 MB (16036029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0e8b6a7e432a7d7e83ae0401587cded3de7b009f60ece49152c5d7e1b9ab7b0`  
		Last Modified: Sat, 16 Oct 2021 02:47:26 GMT  
		Size: 103.5 MB (103549267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60434ee04e102414395ded614f2fcae08a40a03e984196098046b8939f7dba9e`  
		Last Modified: Sat, 16 Oct 2021 02:47:17 GMT  
		Size: 163.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9f0ea5b1133bc466aac94a1232e52a0d089f04ca29ef3902b4b6b54219c57c`  
		Last Modified: Sat, 16 Oct 2021 04:43:18 GMT  
		Size: 4.4 KB (4360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04546f2479ba009a2d16ba3bc7ab68fcc7006a40310b1fc6e495a28a2c9016cc`  
		Last Modified: Sat, 16 Oct 2021 04:43:29 GMT  
		Size: 65.6 MB (65626768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93b79a9632bf969544e9c4c7c27fd5a5f59b100f9d6143e427470627c807965c`  
		Last Modified: Sat, 16 Oct 2021 04:43:24 GMT  
		Size: 114.4 MB (114373764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk8` - linux; arm variant v7

```console
$ docker pull gradle@sha256:4de06cf4184753568bd10f03c02155c39df494ca166a20c4beecc959eb19fee0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **312.6 MB (312612078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6e4d5f6ff3d028d57da70f4102befca26b4b45f2f9acccd828f7bbbc514b2ee`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 16 Oct 2021 01:12:00 GMT
ADD file:625e3906181f4bd86e59a0e9748f67fcb1391a2e65e36c729e71353381a49757 in / 
# Sat, 16 Oct 2021 01:12:00 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 02:38:37 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 02:39:17 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 02:39:18 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Sat, 16 Oct 2021 02:39:39 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f287cdc2a688c2df247ea0d8bfe2863645b73848e4e5c35b02a8a3d2d6b69551';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        armhf|arm)          ESUM='666f159ab0a2dd09c776681eb7cecaf04dc17e35deb213e588fe4f00c2fcac24';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u302b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='c2940f3772d4467a818a0221e80c2c720b6d427a886aaed37262e451ddbb0a56';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='cc13f274becf9dd5517b6be583632819dfd4dd81e524b5c1b4f406bdaf0e063a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 02:39:40 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 02:39:42 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 16 Oct 2021 04:53:04 GMT
CMD ["gradle"]
# Sat, 16 Oct 2021 04:53:04 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 16 Oct 2021 04:53:06 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 16 Oct 2021 04:53:07 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 16 Oct 2021 04:53:07 GMT
WORKDIR /home/gradle
# Sat, 16 Oct 2021 04:53:56 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 16 Oct 2021 04:53:58 GMT
ENV GRADLE_VERSION=7.2
# Sat, 16 Oct 2021 04:53:58 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Sat, 16 Oct 2021 04:54:10 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:8795d4da4abd6abcafe7285749aa85d3a164999e84720a3845f764e56e306771`  
		Last Modified: Sat, 16 Oct 2021 01:15:01 GMT  
		Size: 24.1 MB (24064451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:437a7367762ea761c5abbcde550ac6e83ab2fd882f50cc7c0b8a3ef2bcc5505b`  
		Last Modified: Sat, 16 Oct 2021 02:44:07 GMT  
		Size: 14.9 MB (14902308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:248d7edcc639a6aec37dd2a867f00ccef0d1388ab5fbe6ec4277ec49c7743c57`  
		Last Modified: Sat, 16 Oct 2021 02:44:38 GMT  
		Size: 99.2 MB (99233769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da2c3679bc7b50a86c9e132a87aada4bd8d56370a853126fa9a2dcdf524c16a5`  
		Last Modified: Sat, 16 Oct 2021 02:43:56 GMT  
		Size: 161.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4ed8af1d0f60021440794a51d81808ba12b629b8317fa864fed33eccb86e016`  
		Last Modified: Sat, 16 Oct 2021 05:01:05 GMT  
		Size: 4.4 KB (4352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e4731280e6d87005f17cf27961e455cb92b149b0c7a41e5de3fbf771b3af91d`  
		Last Modified: Sat, 16 Oct 2021 05:01:48 GMT  
		Size: 60.0 MB (60033202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3d8deaa72f90ee922b82651802c62455ac4338703968a28e197e5296500613`  
		Last Modified: Sat, 16 Oct 2021 05:01:38 GMT  
		Size: 114.4 MB (114373835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk8` - linux; arm64 variant v8

```console
$ docker pull gradle@sha256:e5cb47cf39ec5aceb94bfb737331934c1bd859417fe2847e730aab60406e9763
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325480825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84a82da1639930779634c25d1e8c61940c3658bb766e0ae97aaa04beba1c3ee9`
-	Default Command: `["gradle"]`

```dockerfile
# Fri, 01 Oct 2021 02:43:52 GMT
ADD file:e297c32269d46d9846129f357af15b231eb977271968f7f63e65fff73934824b in / 
# Fri, 01 Oct 2021 02:43:52 GMT
CMD ["bash"]
# Fri, 01 Oct 2021 03:02:08 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Fri, 01 Oct 2021 03:29:40 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Fri, 01 Oct 2021 03:29:40 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Thu, 07 Oct 2021 18:41:56 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f287cdc2a688c2df247ea0d8bfe2863645b73848e4e5c35b02a8a3d2d6b69551';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        armhf|arm)          ESUM='666f159ab0a2dd09c776681eb7cecaf04dc17e35deb213e588fe4f00c2fcac24';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u302b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='c2940f3772d4467a818a0221e80c2c720b6d427a886aaed37262e451ddbb0a56';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='cc13f274becf9dd5517b6be583632819dfd4dd81e524b5c1b4f406bdaf0e063a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 07 Oct 2021 18:41:57 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Oct 2021 18:41:58 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Thu, 07 Oct 2021 19:42:35 GMT
CMD ["gradle"]
# Thu, 07 Oct 2021 19:42:35 GMT
ENV GRADLE_HOME=/opt/gradle
# Thu, 07 Oct 2021 19:42:36 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Thu, 07 Oct 2021 19:42:36 GMT
VOLUME [/home/gradle/.gradle]
# Thu, 07 Oct 2021 19:42:36 GMT
WORKDIR /home/gradle
# Thu, 07 Oct 2021 19:42:56 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Thu, 07 Oct 2021 19:42:57 GMT
ENV GRADLE_VERSION=7.2
# Thu, 07 Oct 2021 19:42:57 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Thu, 07 Oct 2021 19:43:02 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:a2e448ef5a4dfc8e290db319d98910aa96a3abfcf38ae90bbac21672b8438d9e`  
		Last Modified: Fri, 01 Oct 2021 02:45:48 GMT  
		Size: 27.2 MB (27172405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04a41a8557fe5edae6e15c9c361239e4a3156f9c03d105c51d28a42e3e13bc82`  
		Last Modified: Fri, 01 Oct 2021 03:33:27 GMT  
		Size: 15.9 MB (15895222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfb2adfe2c9c594dadfa8a640b30c68ad85c0918a312bfc408387ff76ba4b05`  
		Last Modified: Thu, 07 Oct 2021 18:45:44 GMT  
		Size: 102.7 MB (102702114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f864d6773be0b6230c1095197d0f527620b8201102de6d4e5e896f100cd065f9`  
		Last Modified: Thu, 07 Oct 2021 18:45:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582ba2bed86c3fc89e2bd4c5757f15797f4645816bd048bb3c54967b871bd66c`  
		Last Modified: Thu, 07 Oct 2021 19:44:57 GMT  
		Size: 4.4 KB (4366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635709edc0d0eb8e5ac93b6d1415459176f4be07fff68d2aac501c94a7a387f8`  
		Last Modified: Thu, 07 Oct 2021 19:45:09 GMT  
		Size: 65.3 MB (65332814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6898a1a361ec1413be48dab009d13a66e9c212cead320a27dd4eda511375c5e1`  
		Last Modified: Thu, 07 Oct 2021 19:45:05 GMT  
		Size: 114.4 MB (114373744 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `gradle:7-jdk8` - linux; ppc64le

```console
$ docker pull gradle@sha256:7baf7ab462f5f11436bdb310246b9c17a596166d8e8ecf7c98b6cb78af149ad5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **339.9 MB (339946328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e78d526a44885facd106e4170af684d34db5d62bf5e5341b956c83588dff262`
-	Default Command: `["gradle"]`

```dockerfile
# Sat, 16 Oct 2021 00:36:38 GMT
ADD file:9246bf887411af1b286de95d779c11581dcef3c0d5a29e434162f0c085a7ce85 in / 
# Sat, 16 Oct 2021 00:36:44 GMT
CMD ["bash"]
# Sat, 16 Oct 2021 00:54:47 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 16 Oct 2021 00:55:56 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 16 Oct 2021 00:56:03 GMT
ENV JAVA_VERSION=jdk8u302-b08
# Sat, 16 Oct 2021 00:56:18 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='f287cdc2a688c2df247ea0d8bfe2863645b73848e4e5c35b02a8a3d2d6b69551';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_aarch64_linux_hotspot_8u302b08.tar.gz';          ;;        armhf|arm)          ESUM='666f159ab0a2dd09c776681eb7cecaf04dc17e35deb213e588fe4f00c2fcac24';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_arm_linux_hotspot_8u302b08.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='c2940f3772d4467a818a0221e80c2c720b6d427a886aaed37262e451ddbb0a56';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_ppc64le_linux_hotspot_8u302b08.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='cc13f274becf9dd5517b6be583632819dfd4dd81e524b5c1b4f406bdaf0e063a';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u302-b08/OpenJDK8U-jdk_x64_linux_hotspot_8u302b08.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 16 Oct 2021 00:56:24 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 16 Oct 2021 00:56:30 GMT
RUN echo Verifying install ...     && echo javac -version && javac -version     && echo java -version && java -version     && echo Complete.
# Sat, 16 Oct 2021 02:56:08 GMT
CMD ["gradle"]
# Sat, 16 Oct 2021 02:56:11 GMT
ENV GRADLE_HOME=/opt/gradle
# Sat, 16 Oct 2021 02:56:17 GMT
RUN set -o errexit -o nounset     && echo "Adding gradle user and group"     && groupadd --system --gid 1000 gradle     && useradd --system --gid gradle --uid 1000 --shell /bin/bash --create-home gradle     && mkdir /home/gradle/.gradle     && chown --recursive gradle:gradle /home/gradle         && echo "Symlinking root Gradle cache to gradle Gradle cache"     && ln -s /home/gradle/.gradle /root/.gradle
# Sat, 16 Oct 2021 02:56:18 GMT
VOLUME [/home/gradle/.gradle]
# Sat, 16 Oct 2021 02:56:22 GMT
WORKDIR /home/gradle
# Sat, 16 Oct 2021 03:00:14 GMT
RUN apt-get update     && apt-get install --yes --no-install-recommends         fontconfig         unzip         wget                 bzr         git         git-lfs         mercurial         openssh-client         subversion     && rm -rf /var/lib/apt/lists/*         && echo "Testing VCSes"     && which bzr     && which git     && which git-lfs     && which hg     && which svn
# Sat, 16 Oct 2021 03:00:22 GMT
ENV GRADLE_VERSION=7.2
# Sat, 16 Oct 2021 03:00:25 GMT
ARG GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
# Sat, 16 Oct 2021 03:00:40 GMT
# ARGS: GRADLE_DOWNLOAD_SHA256=f581709a9c35e9cb92e16f585d2c4bc99b2b1a5f85d2badbd3dc6bff59e1e6dd
RUN set -o errexit -o nounset     && echo "Downloading Gradle"     && wget --no-verbose --output-document=gradle.zip "https://services.gradle.org/distributions/gradle-${GRADLE_VERSION}-bin.zip"         && echo "Checking download hash"     && echo "${GRADLE_DOWNLOAD_SHA256} *gradle.zip" | sha256sum --check -         && echo "Installing Gradle"     && unzip gradle.zip     && rm gradle.zip     && mv "gradle-${GRADLE_VERSION}" "${GRADLE_HOME}/"     && ln --symbolic "${GRADLE_HOME}/bin/gradle" /usr/bin/gradle         && echo "Testing Gradle installation"     && gradle --version
```

-	Layers:
	-	`sha256:77ba7971d651af68e20e7cbb6603a3f7acd8ef2893066767a93db104723556f2`  
		Last Modified: Sat, 16 Oct 2021 00:38:38 GMT  
		Size: 33.3 MB (33287238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90c930749dacf55e37561edab7967f5a2f51660034fee0da501c2d71cb783301`  
		Last Modified: Sat, 16 Oct 2021 01:03:26 GMT  
		Size: 17.2 MB (17210510 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5eca12d19245c0063ded5121595a0ad4c3a76ddc870b4dfe442ebf32e030c0f`  
		Last Modified: Sat, 16 Oct 2021 01:03:34 GMT  
		Size: 101.1 MB (101072034 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad0b024d35be2de5f53fe8cbd8de0e09181f93aa68af2ebd5376847d137a6608`  
		Last Modified: Sat, 16 Oct 2021 01:03:23 GMT  
		Size: 162.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65d86cf715d9431026b4cf2278726ff877f811fac4d09cf53fe5d345c21c1c21`  
		Last Modified: Sat, 16 Oct 2021 03:10:28 GMT  
		Size: 4.4 KB (4358 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:445aa34fd97e3d1ebfddb15ba35a25acba7d6e23a94178c0f9ea7d30cc331ca9`  
		Last Modified: Sat, 16 Oct 2021 03:10:43 GMT  
		Size: 74.0 MB (73998190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a68c7e38b872206c3c06d351f20a65670a70ef8a082f768e13c992a4008604f`  
		Last Modified: Sat, 16 Oct 2021 03:10:38 GMT  
		Size: 114.4 MB (114373836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
